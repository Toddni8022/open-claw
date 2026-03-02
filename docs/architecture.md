# Code Architecture

This document describes the code structure and design decisions for the OpenClaw project.

## Overview

Both games (`pinball/` and `falling-sand/`) are **single-file HTML5 applications**. All HTML, CSS, and JavaScript live in a single `index.html` file per game. This design choice was made for:

- **Simplicity** — no build tools, no bundlers, no dependencies
- **Portability** — open any `index.html` in a browser and it works
- **GitHub Pages compatibility** — deploy by simply pushing to `main`

---

## Pinball (`pinball/index.html`)

### Architecture Pattern
Game-loop based: `update()` → `draw()` → `requestAnimationFrame(gameLoop)`

### Core Data Structures

```javascript
// Ball state
let ball = { x, y, vx, vy, radius }

// Flipper (left/right)
const flippers = {
  left:  { x, y, length, angle, targetAngle, maxAngle, speed, direction },
  right: { ... }
}

// Bumpers array
const bumpers = [{ x, y, radius, points, hit, color }, ...]

// Targets array (side rails)
const targets = [{ x, y, width, height, points, hit, color }, ...]

// Walls (line segments)
const walls = [{ x1, y1, x2, y2 }, ...]

// Ramps (bonus zones)
const ramps = [{ x, y, width, height, points, label, cooldown }]
```

### Physics Engine

The physics are implemented from scratch with no external libraries:

- **Gravity:** `ball.vy += GRAVITY` each frame
- **Friction:** `ball.vx *= FRICTION`, `ball.vy *= FRICTION`
- **Collision detection:** Point-to-line-segment distance checks for walls and flippers
- **Bounce reflection:** `v_reflected = v - 2(v·n)n` where `n` is the surface normal
- **Flipper force:** When a flipper is actively swinging, applies a fixed directional impulse rather than physical reflection

### Rendering

Canvas 2D API used throughout. Notable techniques:
- **Radial gradients** for bumper and ball shading
- **Shadow blur** for target glow effects
- **Alpha blending** for the drain danger zone

---

## Falling Sand (`falling-sand/index.html`)

### Architecture Pattern
Cellular automaton: update each cell based on neighbors, swap double-buffer grids.

### Core Data Structures

```javascript
// Grid (double-buffered)
let grid = []     // current frame
let nextGrid = [] // next frame being computed

// Cell
{ type: ELEMENT_TYPE, color: cssColorString, updated: boolean }

// Element type constants
const EMPTY = 0, SAND = 1, WATER = 2, FIRE = 3, WOOD = 4,
      PLANT = 5, STONE = 6, OIL = 7, ACID = 8, LAVA = 9,
      ICE = 10, STEAM = 11
```

### Simulation Algorithm

Each frame:
1. **Copy** `grid` to `nextGrid` (reset `updated` flags)
2. **Iterate** from bottom to top (y = ROWS-1 → 0), randomizing horizontal order each row for natural flow
3. **Skip** cells already processed (`nextGrid[y][x].updated`) to prevent double-movement
4. **Dispatch** to element-specific update function (`updateSand`, `updateWater`, etc.)
5. **Swap** `grid` and `nextGrid`

### Element Behaviors

Each element type has a dedicated update function that reads neighboring cells from `grid` (current state) and writes to `nextGrid` (next state):

| Function | Behavior summary |
|----------|-----------------|
| `updateSand` | Falls down; displaces water/oil diagonally |
| `updateWater` | Flows down, then diagonally, then sideways |
| `updateFire` | Rises; randomly dies; spreads to flammables |
| `updateOil` | Like water but floats on water |
| `updateAcid` | Flows like water; probabilistically dissolves neighbors |
| `updateLava` | Flows slowly; ignites flammables; reacts with water/ice |
| `updateIce` | Static; slowly freezes adjacent water |
| `updateSteam` | Rises; randomly condenses back to water or dissipates |
| `updatePlant` | Static; grows when touching water |
| `updateStone`, `updateWood` | Fully static (preserve their position) |

### Rendering

- Grid is 4×4 px per cell (CELL_SIZE = 4)
- Canvas size: 600×500 px → 150×125 cells
- Each non-empty cell is drawn as a filled rectangle with a procedurally generated color variation using HSL

---

## Shared Patterns

Both games use identical patterns:
- **Event-driven input:** `keydown`/`keyup` update a state object; the game loop reads state
- **Touch support:** `touchstart`/`touchmove`/`touchend` events mirror mouse events
- **requestAnimationFrame loop:** Smooth 60 fps rendering tied to display refresh rate
- **localStorage:** Pinball persists `highScore` via `localStorage`

---

## Future Architecture (Roadmap)

As the project grows, shared code may be extracted to `src/`:

```
src/
  js/
    engine/
      physics.js        # Shared physics utilities
      grid.js           # Grid data structure (falling sand)
    utils/
      color.js          # Color generation helpers
  css/
    variables.css       # Shared design tokens
    base.css            # Reset and base styles
```

See [`docs/setup.md`](setup.md) for development environment setup.
