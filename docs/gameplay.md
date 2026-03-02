# Gameplay Documentation

## Pinball

**Play online:** https://toddni8022.github.io/open-claw/pinball/

A fully custom physics-based pinball game built with vanilla JavaScript and HTML5 Canvas.

### Objective

Keep the ball in play as long as possible, hitting bumpers and targets to accumulate points. Increase your score multiplier by hitting all targets in a round.

### Controls

| Key | Action |
|-----|--------|
| `A` or `←` | Left flipper |
| `D` or `→` | Right flipper |
| `Space` (hold & release) | Charge and launch ball |
| `R` | Reset / new game |

### Scoring

| Object | Points |
|--------|--------|
| Small bumpers (green/blue) | 100 |
| Large center bumper (red) | 100 |
| Corner bumpers | 200 |
| Side targets | 250–500 |
| Skill shot (ramp) | 1,000 |

All scores are multiplied by your current **multiplier** (1×–5×).

### Multiplier

Hit the side targets to increase your score multiplier (up to 5×). The multiplier resets when you lose a ball.

### Tips

- **Skill Shot:** Launch the ball with full plunger power to hit the ramp at the top for 1,000 points.
- **Bumper chains:** Aim for tight bumper clusters — ricochets can rack up hundreds of points quickly.
- **Flipper timing:** A flipper actively swinging upward (not stationary) launches the ball with much more force.

---

## Falling Sand

**Play online:** https://toddni8022.github.io/open-claw/falling-sand/

A particle simulation game featuring 10 interacting element types. Draw, combine, and watch the physics unfold.

### Controls

| Key / Input | Action |
|-------------|--------|
| Click / drag | Place selected element |
| `1`–`9`, `0` | Select element (sand, water, fire, wood, plant, stone, oil, acid, lava, ice) |
| `E` | Eraser |
| `C` | Clear all particles |
| `[` | Decrease brush size |
| `]` | Increase brush size |
| Brush size slider | Adjust brush size (1–15) |

### Elements

| Element | Behavior |
|---------|----------|
| **Sand** | Falls, displaces water and oil |
| **Water** | Flows, spreads horizontally |
| **Fire** | Rises, spreads to flammable materials, melts ice |
| **Wood** | Static; burns when touching fire or lava |
| **Plant** | Static; grows when touching water |
| **Stone** | Fully static; immune to acid |
| **Oil** | Flows; floats on water; highly flammable |
| **Acid** | Flows; dissolves most elements (not stone/lava) |
| **Lava** | Flows slowly; ignites flammables; cools to stone on contact with water |
| **Ice** | Static; freezes nearby water; melts to water near fire/lava |

### Interesting Combinations

- **Water + Fire** → Steam
- **Lava + Water** → Stone
- **Lava + Ice** → Water
- **Fire + Wood/Oil/Plant** → Spreads fire
- **Acid + (almost anything)** → Dissolves it
- **Ice + Water** → Slowly freezes nearby water

### Tips

- Build a **container** with stone, then fill it with water and add fire from the top to watch steam rise.
- Drop **sand** into water to see it displace the liquid.
- Create **chain reactions** by placing oil next to lava.
