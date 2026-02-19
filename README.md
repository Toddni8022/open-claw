# HAL — Personal AI Workspace (OpenClaw + Kali Linux)

HAL is a personal AI assistant workspace built on [OpenClaw](https://openclaw.ai), running on Kali Linux. This repo contains HAL's live configuration, persistent memory, and two browser games built entirely through human-AI collaboration.

Built by **Todd Nicholas** and HAL.

---

## Live Projects

Two fully playable browser games built from scratch using only Claude + OpenClaw — no game libraries, no frameworks, just vanilla JavaScript and HTML5 Canvas:

| Game | Link | Description |
|------|------|-------------|
| Pinball | [Play](https://toddni8022.github.io/open-claw/pinball/) | Physics engine, dual flippers, bumpers, scoring multipliers |
| Falling Sand | [Play](https://toddni8022.github.io/open-claw/falling-sand/) | 10 interacting particle types: sand, water, fire, lava, acid, ice, and more |

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

### Games
- `pinball/` — Full pinball game with physics engine
- `falling-sand/` — Particle simulation with 10 element types

---

## Tech Stack

- **Platform:** OpenClaw + Claude (Anthropic)
- **Games:** Vanilla JavaScript, HTML5 Canvas
- **Physics:** Custom-built (no external libraries)
- **OS:** Kali Linux

---

## Related

- [-Open-Claw-windows-11](https://github.com/Toddni8022/-Open-Claw-windows-11) — Windows 11 setup guide for OpenClaw
- [OpenClaw Official](https://openclaw.ai)
