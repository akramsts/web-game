# Gree Runner

An endless 2D running game built with plain HTML, CSS, and JavaScript. Jump over obstacles, chain perfect jumps for bonus points, and try to beat your high score. Installable as a PWA so it can be played offline like a native app.

## Play

**Live demo:** [akramsts.github.io/web-game](https://akramsts.github.io/web-game/)

You can also open `index.html` directly in any modern browser to play locally.

## Features

- Endless runner gameplay with procedurally spawned obstacles (four types: normal, short, fat, tall)
- Increasing difficulty: game speed ramps up as your score grows
- Perfect jump streak system that rewards well-timed high jumps with bonus points
- Score milestones with on-screen callouts at 100, 200, 500, 800, and 1200 points
- Persistent high score, saved locally in the browser
- Three visual themes: Obsidian, Amber, and Platinum
- Procedural sound effects and background music generated with the Web Audio API, with a mute toggle
- Pause and resume at any time
- Fully responsive layout with touch, mouse, and keyboard controls
- Installable Progressive Web App (PWA) with offline support via a service worker

## Controls

| Action | Input |
|---|---|
| Jump | `Space`, `Arrow Up`, tap, or click |
| Pause / Resume | `P` |
| Mute / Unmute sound | `M` |
| Restart | `Enter` |

## Tech Stack

- HTML5, CSS3, vanilla JavaScript (no frameworks or build step)
- Web Audio API for sound generation
- Service Worker + Web App Manifest for PWA/offline support

## Project Structure

```
.
├── index.html       # Game markup, styles, and logic
├── manifest.json     # PWA manifest (name, icons, theme)
├── sw.js              # Service worker for offline caching
├── icon-192.png     # App icon (192x192)
└── icon-512.png     # App icon (512x512)
```

## Running Locally

No build tools or dependencies are required.

```bash
git clone https://github.com/akramsts/web-game.git
cd web-game
```

Then simply open `index.html` in your browser. For full PWA/service worker behavior (which requires a proper origin rather than the `file://` protocol), serve the folder locally, for example:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

## Installing as an App

Once served over `http` or `https`, most browsers will offer an "Install" or "Add to Home Screen" option, letting you play Gree Runner as a standalone app, online or off.

## License

This project is open source. Feel free to fork it, modify it, and make it your own.

## Author

Made by **Akram**
