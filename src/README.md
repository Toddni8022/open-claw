# src/

This directory contains source files for future modular development.

## Structure

- `js/` — Shared JavaScript modules (utility functions, game engine components)
- `css/` — Shared CSS stylesheets and design tokens
- `assets/` — Images, audio files, and other static assets

## Current Architecture

The current games (`pinball/` and `falling-sand/`) are self-contained single-file HTML applications that embed all CSS and JavaScript inline. This was done for simplicity and GitHub Pages compatibility.

Future development may extract shared code (physics engine, rendering utilities) into this `src/` directory as ES modules.

See [`docs/architecture.md`](../docs/architecture.md) for more details.
