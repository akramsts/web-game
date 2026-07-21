# Gree Runner

Gree Runner is a compact endless runner built with vanilla HTML, CSS, and JavaScript. Jump over obstacles, chain perfect clears for bonus points, switch themes, and compete against your local best score. The game supports keyboard, mouse, and touch input, and it works offline as a Progressive Web App.

## Table of Contents

- [Features](#features)
- [How to Play](#how-to-play)
- [Getting Started](#getting-started)
- [Install as an App](#install-as-an-app)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Customization](#customization)
- [License](#license)

## Features

- Endless 2D runner gameplay with smooth acceleration
- Perfect jump streaks for extra bonus points
- Milestone notifications at 100, 200, 500, 800, and 1200 points
- Persistent high score, theme, and sound settings via `localStorage`
- Three built-in themes: Obsidian, Amber, and Platinum
- Synthesized retro sound effects using the Web Audio API
- Pause/resume controls for easier gameplay
- Keyboard, mouse, and touch controls for desktop and mobile
- Offline support through service worker caching

## How to Play

Avoid obstacles while keeping your run alive. Your score increases automatically over time, and clean jumps can earn you more points.

**Controls**

- Jump: `Space`, `↑`, click, or tap
- Pause / Resume: `P`
- Mute / Unmute Sound: `M`
- Start / Restart: `Enter` or the on-screen button

## Getting Started

No build tools or external dependencies are required.

### Option 1: Open directly
Open `index.html` in a modern browser.

### Option 2: Serve locally (recommended)
For full PWA behavior, run a local web server instead of opening the file directly.

```bash
# Using Python
python3 -m http.server 8000

# Using Node
npx serve .
```

Then visit `http://localhost:8000`.

## Install as an App
When served from `http://localhost` or `https://`, supported browsers may prompt to install the game. Install it to play in standalone mode with offline support.

## Project Structure

```
.
├── index.html     # Game UI, styling, and logic
├── manifest.json  # PWA manifest metadata and icons
├── sw.js          # Service worker for offline caching
├── icon-192.png   # PWA icon (192x192)
└── icon-512.png   # PWA icon (512x512)
```

## Tech Stack

- HTML5 / CSS3 for gameplay UI and responsive styling
- Vanilla JavaScript for the game loop and mechanics
- Web Audio API for synth sound effects
- `localStorage` for best score, theme, and audio settings
- Service Worker + Web App Manifest for offline PWA support

## Customization

- Themes: edit the `THEMES` object in `index.html`
- Difficulty: adjust `GRAVITY`, `BASE_SPEED`, and `MAX_EXTRA_SPEED`
- Obstacle timing: change the spawn timing logic in `spawnNewObstacle()`
- Branding: replace `icon-192.png`, `icon-512.png`, and update `manifest.json`

## License

MIT

---

Enjoy the run and try to beat your high score!