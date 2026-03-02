# OpenClaw — Browser Games & AI Workspace

[![CI](https://github.com/Toddni8022/open-claw/actions/workflows/ci.yml/badge.svg)](https://github.com/Toddni8022/open-claw/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **HAL** is a personal AI assistant workspace built on [OpenClaw](https://openclaw.ai), running on Kali Linux. This repo contains HAL's live configuration, persistent memory, and two browser games built entirely through human-AI collaboration.
>
> Built by **Todd Nicholas** and HAL.

---

## Table of Contents

- [Live Demo](#live-demo)
- [Features](#features)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Game Controls](#game-controls)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Browser Compatibility](#browser-compatibility)
- [What's in This Repo](#whats-in-this-repo)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [Related](#related)
- [License](#license)

---

## Live Demo

Two fully playable browser games — no installation, no plugins, just click and play:

| Game | Link | Description |
|------|------|-------------|
| 🎰 Pinball | [**Play Now**](https://toddni8022.github.io/open-claw/pinball/) | Physics engine, dual flippers, bumpers, scoring multipliers |
| 🏜️ Falling Sand | [**Play Now**](https://toddni8022.github.io/open-claw/falling-sand/) | 10 interacting particle types: sand, water, fire, lava, acid, ice, and more |

---

## Features

### Pinball
- Custom physics engine (gravity, friction, realistic bounce)
- Dual flippers with momentum-based ball launching
- 6 bumpers, 4 side targets, slingshots, and a skill-shot ramp
- Score multiplier system (1×–5×)
- High score persistence via `localStorage`
- Touch screen support

### Falling Sand
- 10 particle types with unique interactions: sand, water, fire, wood, plant, stone, oil, acid, lava, ice
- Steam as an emergent particle (water + fire/lava → steam)
- Adjustable brush size (1–15 cells)
- Keyboard shortcuts for element selection
- Touch screen support
- Particle count display

---

## Screenshots

<!-- Add screenshots here once available -->
> 📸 Screenshots coming soon. [Play the games live](https://toddni8022.github.io/open-claw/) to see them in action.

---

## Getting Started

### Prerequisites

- A modern web browser (see [Browser Compatibility](#browser-compatibility))
- [Node.js](https://nodejs.org/) v18+ (only needed for development/linting)

### Play Instantly

Just open the HTML files directly in your browser — no build step, no server required:

```bash
open pinball/index.html
open falling-sand/index.html
```

### Development Setup

```bash
# Clone the repo
git clone https://github.com/Toddni8022/open-claw.git
cd open-claw

# Install dev dependencies (linters)
npm install

# Start a local dev server
npm start
```

See [`docs/setup.md`](docs/setup.md) for the full development guide.

---

## Game Controls

### Pinball

| Key | Action |
|-----|--------|
| `A` / `←` | Left flipper |
| `D` / `→` | Right flipper |
| `Space` (hold & release) | Charge and launch ball |
| `R` | Reset game |

### Falling Sand

| Key | Action |
|-----|--------|
| `1`–`9`, `0` | Select element |
| `E` | Eraser |
| `C` | Clear all |
| `[` / `]` | Decrease / increase brush size |

See [`docs/gameplay.md`](docs/gameplay.md) for full gameplay documentation.

---

## Project Structure

```
open-claw/
├── pinball/              # 🎰 Pinball game
│   └── index.html
├── falling-sand/         # 🏜️ Falling Sand simulation
│   └── index.html
├── src/                  # Future shared source files
│   ├── js/               #   JavaScript modules
│   ├── css/              #   Stylesheets
│   └── assets/           #   Images, audio
├── public/               # Static public files
├── docs/                 # Documentation
│   ├── setup.md          #   Development setup
│   ├── gameplay.md       #   Game controls & rules
│   ├── architecture.md   #   Code architecture
│   └── contributing.md   #   How to contribute
├── tests/                # Automated tests (planned)
├── .github/
│   ├── workflows/ci.yml  #   CI pipeline
│   └── ISSUE_TEMPLATE/   #   Bug & feature templates
├── package.json
├── .eslintrc.json
├── .editorconfig
├── .prettierrc
├── CONTRIBUTING.md
├── CHANGELOG.md
└── LICENSE
```

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Games | Vanilla JavaScript, HTML5 Canvas |
| Physics | Custom-built (zero dependencies) |
| Styling | Plain CSS (inline) |
| Platform | OpenClaw + Claude (Anthropic) |
| Hosting | GitHub Pages |
| CI/CD | GitHub Actions |
| Linting | ESLint, HTMLHint |
| OS | Kali Linux |

---

## Browser Compatibility

| Browser | Status |
|---------|--------|
| Chrome / Edge 90+ | ✅ Fully supported |
| Firefox 88+ | ✅ Fully supported |
| Safari 14+ | ✅ Fully supported |
| Mobile Chrome / Safari | ✅ Touch controls supported |
| IE 11 | ❌ Not supported |

---

## What's in This Repo

### Agent Configuration Files

| File | Purpose |
|------|---------|
| `SOUL.md` | HAL's personality, values, and communication style |
| `MEMORY.md` | Long-term memory — what HAL remembers across sessions |
| `IDENTITY.md` | Core identity definition |
| `HEARTBEAT.md` | Health monitoring and activity tracking |
| `AGENTS.md` | Workspace protocols and agent rules |
| `TOOLS.md` | Available tools and how to use them |
| `USER.md` | Todd's preferences and profile |
| `BOOTSTRAP.md` | Session initialization instructions |

### Session Logs

Daily session logs are stored in `memory/YYYY-MM-DD.md` to maintain continuity between conversations.

---

## Roadmap

- [ ] Landing page (`index.html`) linking to both games
- [ ] Mobile-optimized on-screen flipper buttons for Pinball
- [ ] New particle types for Falling Sand (gunpowder, steam vents, glass)
- [ ] High score leaderboard (Pinball)
- [ ] Sound effects
- [ ] Extract shared JS into `src/` as ES modules
- [ ] Automated browser tests with Playwright

---

## Contributing

Contributions, bug reports, and feature requests are welcome!

1. Read the [Contributing Guide](CONTRIBUTING.md)
2. Open an [issue](https://github.com/Toddni8022/open-claw/issues) to discuss your idea
3. Fork, branch, and open a pull request

---

## Related

- [-Open-Claw-windows-11](https://github.com/Toddni8022/-Open-Claw-windows-11) — Windows 11 setup guide for OpenClaw
- [OpenClaw Official](https://openclaw.ai)

---

## License

[MIT](LICENSE) © 2026 Todd Nicholas
