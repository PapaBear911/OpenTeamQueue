# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- **Run locally**: Open `index.html` directly in browser or serve via static file server (e.g., `python -m http.server 8000` or `npx serve .`). Use `http://localhost` (not LAN IP) for microphone/Web Speech API functionality.
- **Lint / Build / Test**: None. Zero-build architecture. Verify syntax and logic directly in browser developer tools or Node (`node -c index.html` will fail on HTML, test vanilla scripts via node/browser).

## Architecture

- **Single-File Zero-Build**: Entire markup, CSS, and vanilla ES6 JavaScript live in `index.html`. Do not introduce bundlers, build steps, or package managers.
- **Dependencies**: CDN only (e.g. `anime.min.js`, Google Fonts).
- **Layout & Styling**: Uses `@layer od-layout` primitives (`.od-stack`, `.od-row`, `.od-grid`, `.od-rail`) and `:root` theme variables (`--bg`, `--surface`, `--accent`, `--border`).
- **State & Storage**: Global in-memory state (`players`, `courts`, `gameList`, `roundPrefs`, `fees`) persists to `localStorage['openteamqueue_db']` via `getDB()`, `putDB()`, and `save()`. Session schema contains `sessions` and `current`.
- **DOM Access**: Elements accessed via `$('elementId')` (`const $ = id => document.getElementById(id);`).
- **Simplifications**: Mark intentional ceilings or upgrade paths with `// ponytail: <ceiling; upgrade path>`.
