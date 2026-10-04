# Project Guidelines

Single static file web application. See [README.md](README.md) for run and deployment details.

## Code Style & Architecture

- **Zero-build single file**: All markup, CSS, and vanilla ES6 JavaScript live in `index.html`. Do not introduce bundlers, build steps, or package managers unless explicitly requested.
- **Styling**: Structural layout uses `@layer od-layout` primitives (`.od-stack`, `.od-row`, `.od-grid`, `.od-rail`). Visual styles consume `:root` CSS variables (`--bg`, `--surface`, `--accent`, `--border`).
- **External dependencies**: CDN only (`anime.min.js`, Google Fonts).
- **State & persistence**: Global runtime state (`players`, `courts`, `gameList`, `roundPrefs`, `fees`) persists to `localStorage['openteamqueue_db']` via `getDB()`, `putDB()`, and `save()`.
- **DOM conventions**: Elements accessed via `$('elementId')` (`const $ = id => document.getElementById(id);`). Verify ID existence when adding or modifying controls.
- **Simplifications**: Mark intentional ceilings or upgrade paths with `// ponytail: <ceiling; upgrade path>`.

## Development & Verification

- **Run**: Open `index.html` directly or serve over HTTP (`http://localhost` required for Web Speech / microphone APIs).
- **Test**: Verify syntax, DOM element bindings, and state integrity in browser or console. Avoid breaking `localStorage` session schema (`sessions`, `current`).
