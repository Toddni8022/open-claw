# Contributing to OpenClaw

Thank you for your interest in contributing to OpenClaw! This document explains how to get involved.

## Ways to Contribute

- 🐛 **Report bugs** — open an [issue](https://github.com/Toddni8022/open-claw/issues/new/choose)
- 💡 **Suggest features** — open a [feature request](https://github.com/Toddni8022/open-claw/issues/new/choose)
- 🔧 **Fix bugs** — fork, fix, and submit a pull request
- 📖 **Improve docs** — typos, clarity, new examples
- 🎮 **Add game elements** — new particle types, physics features

## Getting Started

1. **Fork** the repository on GitHub
2. **Clone** your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/open-claw.git
   cd open-claw
   ```
3. **Install** dev dependencies:
   ```bash
   npm install
   ```
4. **Create a branch** for your change:
   ```bash
   git checkout -b feature/my-new-feature
   ```

See [`docs/setup.md`](setup.md) for full development environment instructions.

## Making Changes

- Keep changes focused — one feature or fix per pull request
- Follow the existing code style (`.editorconfig` and `.eslintrc.json` enforce this)
- Test your changes in Chrome, Firefox, and Safari if possible
- Run linting before submitting:
  ```bash
  npm run lint
  ```

## Submitting a Pull Request

1. Push your branch to your fork
2. Open a pull request against `main`
3. Fill in the pull request template
4. Describe what you changed and why
5. Link any related issues (`Fixes #123`)

## Code Style

- **Indentation:** 4 spaces (no tabs)
- **Quotes:** Single quotes for JavaScript strings
- **Semicolons:** Required
- **Line length:** Max 100 characters
- **Trailing commas:** ES5-style (objects/arrays, not function params)

These are enforced by `.eslintrc.json` and `.prettierrc`.

## Questions?

Open a [discussion](https://github.com/Toddni8022/open-claw/discussions) or file an issue — happy to help!
