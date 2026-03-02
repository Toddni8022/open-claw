# Tests

This directory is reserved for automated tests.

## Current Status

The games (`pinball/` and `falling-sand/`) are self-contained HTML5 Canvas applications with no external dependencies, making traditional unit testing less straightforward. Integration and end-to-end testing are planned for future development.

## Planned Testing Approaches

### Unit Tests
For any shared JavaScript modules extracted to `src/js/`, use a test runner such as:
- [Vitest](https://vitest.dev/) — fast, ESM-native
- [Jest](https://jestjs.io/) — widely used, good ecosystem

Example structure:
```
tests/
  unit/
    physics.test.js    # test physics engine functions
    grid.test.js       # test grid utilities (falling sand)
  integration/
    game-loop.test.js
```

### End-to-End Tests
For browser-level testing, consider:
- [Playwright](https://playwright.dev/) — multi-browser automation
- [Cypress](https://www.cypress.io/) — great for canvas-based games

### Running Tests

Once tests are added, run them with:
```bash
npm test
```

## Contributing Tests

See [`CONTRIBUTING.md`](../CONTRIBUTING.md) for guidelines on writing and submitting tests.
