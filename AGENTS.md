# AGENTS.md

## Cursor Cloud specific instructions

This is a single-file static web application (`index.html`) with no build system, package manager, or backend. It loads two CDN dependencies at runtime: `dom-to-image` (cdnjs) and Google Fonts (`Onest`).

### Running the app

Serve the project root with any static HTTP server:

```bash
npx serve -l 3000 /workspace
```

Then open `http://localhost:3000/` in Chrome.

### Key notes

- There is no `package.json`, no build step, no linter config, and no test framework in this repo.
- The app requires internet access for CDN resources (`dom-to-image` and Google Fonts). Without internet, PNG export and the default font will not work.
- The entire UI is in Russian.
- The app has two modes: "Готовый макет" (import SVG) and "Генератор" (build sticker from text). Both apply 3D perspective transforms and support PNG/SVG export.
