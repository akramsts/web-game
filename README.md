# Gree Runner

An endless 2D running game built with plain HTML, CSS, and JavaScript. Jump over obstacles, survive as long as you can, and try to beat your high score. It is installable as a PWA, so you can play it offline like a native app.

## Play

**Live demo:** [akramsts.github.io/web-game](https://akramsts.github.io/web-game/)

You can also open `index.html` directly in any modern browser to play locally.

## Features

- Endless runner gameplay with randomly spawned obstacles (four types: normal, short, fat, and tall)
- Increasing difficulty: the game speeds up the longer you survive, with no speed limit
- Score milestones with on-screen callouts at 100, 200, 500, 800, and 1200 points
- Persistent high score, saved locally in the browser
- Three visual themes: Obsidian, Amber, and Platinum
- Sound effects and background music generated with the Web Audio API, with a mute toggle
- Pause and resume at any time, with auto-pause when you switch tabs or leave the window and a 3-2-1 countdown on resume
- Fully responsive layout with touch, mouse, and keyboard controls
- Installable Progressive Web App (PWA) with offline support via a service worker

## Controls

| Action | Input |
|---|---|
| Jump | `Space`, `Arrow Up`, tap, or click |
| Pause / Resume | `P` |
| Mute / Unmute sound | `M` |
| Start / Restart | `Enter` |

## Tech Stack

- HTML5, CSS3, and vanilla JavaScript (no frameworks or build step)
- Web Audio API for sound generation
- Service worker and web app manifest for PWA and offline support

## Project Structure

```
.
├── index.html      # Game markup, styles, and logic
├── manifest.json   # PWA manifest (name, icons, theme)
├── sw.js           # Service worker for offline caching
├── icon-192.png    # App icon (192x192)
├── icon-512.png    # App icon (512x512)
└── README.md
```

## Running Locally

No build tools or dependencies are required.

```bash
git clone https://github.com/akramsts/web-game.git
cd web-game
```

Then open `index.html` in your browser. The service worker needs a proper origin rather than the `file://` protocol, so for full PWA behavior, serve the folder locally. For example:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

## Installing as an App

Once the game is served over `http` or `https`, most browsers offer an "Install" or "Add to Home Screen" option, so you can play Gree Runner as a standalone app, online or offline.

## License

This project is open source. Feel free to fork it, modify it, and make it your own.

## Author

Made by **Akram**