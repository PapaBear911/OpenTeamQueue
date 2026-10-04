# OpenTeamQueue 🏸

> Zero-build sports queuing, scoreboard, and tournament management app for badminton, pickleball, and tennis.

Live single-page web app built with vanilla HTML, CSS, and modern JavaScript. Runs directly in any modern browser with no build step, bundler, or server required.

## Features

- **Queue & Court Management**: Dynamic queue randomizer, court assignment, and waitlist tracking.
- **Live Scoreboard**: Real-time score counter, match timer, and game history.
- **Tournament Formats**: Round robin, brackets, and custom group stages.
- **Session & Fee Tracker**: Automatic fee splitting, attendance, and player stats.
- **Offline & Local First**: State persists in `localStorage`.
- **Zero Build**: Single-file architecture (`index.html`).

## Getting Started

### Local

Simply open `index.html` in your web browser:

```bash
# Direct open
open index.html        # macOS
start index.html       # Windows

# Or via a lightweight local server
python -m http.server 8000
# or
npx serve .
```

> **Note**: Access via `http://localhost` if using Web Speech / microphone features.

### GitHub Pages Deployment

1. Push this repository to GitHub.
2. Navigate to **Settings** > **Pages**.
3. Under **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click **Save**.

## Tech Stack

- Vanilla HTML5 / ES6 JavaScript
- Modern CSS (CSS Layers, Custom Properties)
- [Anime.js](https://animejs.com/) (CDN)
- Google Fonts

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
