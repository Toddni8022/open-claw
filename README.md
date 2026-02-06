# 🔴 HAL - Personal AI Assistant Workspace

A self-hosted AI assistant configuration built on [OpenClaw](https://github.com/openclaw/openclaw), featuring custom personality, persistent memory, and interactive web applications.

### 🎮 Live Demos
> **[Play Pinball](https://toddni8022.github.io/open-claw/pinball/)** | **[Play Falling Sand](https://toddni8022.github.io/open-claw/falling-sand/)**

## Overview

This repository contains my personal AI workspace — a fully configured assistant named HAL (yes, after *that* HAL) with persistent memory across sessions, custom behavioral guidelines, and interactive projects built through human-AI collaboration.

### What's Here

| Directory/File | Description |
|----------------|-------------|
| `pinball/` | Browser-based pinball game with physics engine |
| `falling-sand/` | Particle simulation with 10 interacting elements |
| `memory/` | Daily session logs for context continuity |
| `SOUL.md` | AI personality and behavioral guidelines |
| `MEMORY.md` | Long-term curated memory |
| `AGENTS.md` | Workspace conventions and protocols |

## 🎮 Interactive Projects

### Pinball
A complete browser-based pinball game featuring:
- **Real-time physics** — gravity, momentum, collision detection, bounce damping
- **Game mechanics** — dual flippers, charged plunger, 6 bumpers, 4 targets
- **Scoring system** — multipliers up to 5x, high score persistence
- **Controls** — A/D or Arrow keys for flippers, Space to launch

**[▶️ Play Pinball](https://toddni8022.github.io/open-claw/pinball/)** — runs in any modern browser.

### Falling Sand
A particle simulation sandbox where different elements interact:
- **10 Elements** — Sand, Water, Fire, Wood, Plant, Stone, Oil, Acid, Lava, Ice
- **Realistic behaviors** — fire spreads to flammables, water flows, acid dissolves
- **Element interactions** — lava + water = stone, ice freezes water, oil floats
- **Touch-friendly** — works on mobile devices

**[▶️ Play Falling Sand](https://toddni8022.github.io/open-claw/falling-sand/)** — click and drag to paint elements.

## 🧠 AI Configuration

This workspace demonstrates a **memory-persistent AI assistant** architecture:

```
┌─────────────────────────────────────────────┐
│              OpenClaw Gateway               │
├─────────────────────────────────────────────┤
│  SOUL.md          → Personality & behavior  │
│  MEMORY.md        → Long-term memory        │
│  memory/YYYY-MM-DD.md → Daily session logs  │
│  AGENTS.md        → Workspace protocols     │
│  USER.md          → User context            │
└─────────────────────────────────────────────┘
```

### Key Features
- **Session continuity** — AI reads memory files at session start
- **Authentic personality** — configured for direct, competent responses (no corporate speak)
- **Proactive capabilities** — can check emails, calendars, and perform background tasks
- **Tool integration** — browser automation, file management, shell access

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| AI Platform | [OpenClaw](https://openclaw.ai) |
| Language Model | Claude (Anthropic) |
| Frontend Games | Vanilla JavaScript, HTML5 Canvas |
| Physics | Custom implementation (no libraries) |
| Version Control | Git + GitHub CLI |

## 🚀 Getting Started

### Run the Games
No build step required — just open the HTML files in a browser:
```bash
# Pinball
open pinball/index.html

# Falling Sand
open falling-sand/index.html
```

### Set Up Your Own AI Workspace
1. Install [OpenClaw](https://docs.openclaw.ai)
2. Clone this repo to your workspace directory
3. Customize `SOUL.md` and `USER.md` for your preferences
4. Start chatting — the AI will read and update memory files automatically

## 📁 Project Structure

```
.
├── README.md           # This file
├── LICENSE             # MIT License
├── pinball/
│   └── index.html      # Complete pinball game (27KB)
├── falling-sand/
│   └── index.html      # Particle simulation (27KB)
├── memory/
│   └── 2026-02-06.md   # Daily session logs
├── AGENTS.md           # Workspace conventions
├── SOUL.md             # AI personality config
├── MEMORY.md           # Persistent AI memory
├── USER.md             # User preferences
├── IDENTITY.md         # AI identity (name, emoji, vibe)
├── TOOLS.md            # Local tool configurations
└── HEARTBEAT.md        # Periodic task checklist
```

## 🎯 Why This Exists

This project demonstrates:
- **Human-AI collaboration** — real projects built through conversation
- **Prompt engineering** — structured personality and behavior configuration
- **Self-hosted AI** — running personal assistants with privacy and control
- **Rapid prototyping** — functional games built in single sessions

## 📜 License

MIT License — see [LICENSE](LICENSE) for details.

---

*Built with [OpenClaw](https://openclaw.ai) • Powered by Claude • Created 2026*
