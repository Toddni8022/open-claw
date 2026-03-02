# Development Setup

This guide explains how to set up the OpenClaw project locally for development.

## Prerequisites

- **Node.js** v18 or higher ([download](https://nodejs.org/))
- **npm** v9 or higher (bundled with Node.js)
- A modern web browser (Chrome, Firefox, Edge, or Safari)
- A code editor (VS Code recommended)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Toddni8022/open-claw.git
   cd open-claw
   ```

2. **Install development dependencies:**
   ```bash
   npm install
   ```

## Running Locally

The games are plain HTML5 files — no build step required. You can open them directly in a browser or use a local server.

### Option 1: Open directly
```bash
# Open the pinball game
open pinball/index.html

# Open the falling sand game
open falling-sand/index.html
```

### Option 2: Local dev server (recommended)
```bash
npm start
# Opens a local server at http://localhost:3000
```

Then navigate to:
- [http://localhost:3000/pinball/](http://localhost:3000/pinball/)
- [http://localhost:3000/falling-sand/](http://localhost:3000/falling-sand/)

## Linting

Run all linters:
```bash
npm run lint
```

Run individually:
```bash
npm run lint:html   # HTML validation
npm run lint:js     # JavaScript linting (ESLint)
```

## Editor Setup

### VS Code (Recommended Extensions)
- **ESLint** (`dbaeumer.vscode-eslint`) — JS linting in editor
- **Prettier** (`esbenp.prettier-vscode`) — auto-formatting
- **EditorConfig** (`editorconfig.editorconfig`) — consistent code style
- **HTMLHint** (`mkaufman.htmlhint`) — HTML validation

The repo includes `.editorconfig`, `.eslintrc.json`, and `.prettierrc` which configure these automatically.

## Project Structure

```
open-claw/
├── pinball/            # Pinball game
│   └── index.html
├── falling-sand/       # Falling Sand particle sim
│   └── index.html
├── src/                # Future shared source files
│   ├── js/
│   ├── css/
│   └── assets/
├── public/             # Static public files
├── docs/               # Documentation
├── tests/              # Automated tests
└── .github/            # GitHub workflows and templates
```

See [`architecture.md`](architecture.md) for more detail on the code structure.

## Deployment

The project is deployed via **GitHub Pages** from the `main` branch. Pushing to `main` automatically updates the live site at:
- https://toddni8022.github.io/open-claw/pinball/
- https://toddni8022.github.io/open-claw/falling-sand/
