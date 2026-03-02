# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [Unreleased]

### Added
- `package.json` with project metadata and lint/test scripts
- `.editorconfig` for consistent code style across editors
- `.eslintrc.json` for JavaScript linting configuration
- `.prettierrc` for code formatting configuration
- `docs/` directory with setup, gameplay, architecture, and contributing guides
- `tests/` directory with testing guide
- `src/` directory scaffold for future modular source files
- `public/` directory scaffold for static public files
- `.github/workflows/ci.yml` — CI pipeline (HTML validation, JS linting, link checking)
- `.github/ISSUE_TEMPLATE/bug_report.md` — bug report template
- `.github/ISSUE_TEMPLATE/feature_request.md` — feature request template
- `.github/PULL_REQUEST_TEMPLATE.md` — pull request template
- `CONTRIBUTING.md` — contribution guide
- `CHANGELOG.md` — this file

### Changed
- Enhanced `README.md` with badges, table of contents, features, screenshots placeholder, browser compatibility, roadmap, and full documentation links
- Updated `.gitignore` with Node.js, build artifact, and additional OS/editor patterns

---

## [1.0.0] — 2026-02-06

### Added
- **Pinball game** (`pinball/index.html`) — physics engine, dual flippers, bumpers, targets, slingshots, ramps, score multipliers, high score persistence
- **Falling Sand simulation** (`falling-sand/index.html`) — 10 interacting particle types: sand, water, fire, wood, plant, stone, oil, acid, lava, ice (plus steam)
- `README.md` — project overview and live links
- `LICENSE` — MIT license
- `.gitignore` — OS and editor exclusions
- `SOUL.md`, `MEMORY.md`, `IDENTITY.md`, `HEARTBEAT.md`, `AGENTS.md`, `TOOLS.md`, `USER.md`, `BOOTSTRAP.md` — HAL AI workspace configuration files
