# RallyQueue

Session-based queuing for Badminton, Pickleball & Tennis — single static file, no build step.

- Partner roulette + match rotation (doubles / singles, BYE handling)
- Scoreboard with scorekeeper pad, finish/reopen lifecycle
- Court management, fee management, session + global leaderboards
- Sessions persist in browser `localStorage`, with JSON export/import backup

## Run locally

Just open `index.html` in a browser (use `http://localhost`, not a LAN IP, for microphone/speech-to-text).

## Host on GitHub Pages

Settings → Pages → Deploy from branch → `main` / root. App goes live at `https://<user>.github.io/BadmintonTeamQueuing/`.
