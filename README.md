# Gree Runner

A slick, endless 2D runner game — built with nothing but HTML, CSS, and vanilla JavaScript. Jump over obstacles, chain "perfect" jumps for bonus points, and chase your high score. Installable as a Progressive Web App (PWA) so it works offline and runs like a native app.

![Platform](https://img.shields.io/badge/platform-web-blue)
![PWA](https://img.shields.io/badge/PWA-ready-22c55e)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

## Features

- **Endless procedural gameplay** — obstacles spawn continuously, and speed ramps up the longer you survive
- **Perfect jump streaks** — clear an obstacle with enough height for a "perfect" jump, and chain them for multiplying bonus points
- **Milestone callouts** — fun pop-up messages at score milestones (100, 200, 500, 800, 1200+)
- **Persistent high score** — saved locally in your browser, no account needed
- **3 built-in themes** — Obsidian, Amber, and Platinum, saved to your preferences
- **Retro sound effects** — procedurally generated with the Web Audio API (jump, perfect, background beat), fully mutable
- **Pause / resume support**
- **Keyboard, mouse, and touch controls** — playable on desktop and mobile
- **Installable PWA** — add it to your home screen and play offline via service worker caching

## How to Play

Avoid the incoming obstacles for as long as you can. Your score climbs automatically over time, and jumping cleanly over an obstacle at height builds a **perfect streak** for bonus points.

| Action | Control |
|---|---|
| Jump | `Space`, `↑`, click, or tap |
| Pause / Resume | `P` |
| Mute / Unmute Sound | `M` |
| Start / Restart | `Enter` or the on-screen button |

## Getting Started

No build tools, no dependencies, no installation required.

### Option 1: Open directly
Just open `index.html` in any modern browser.

### Option 2: Serve locally (recommended, needed for full PWA behavior)
Service workers require a proper origin (not `file://`), so serve the folder with any static server:

```bash
# Using Python
python3 -m http.server 8000

# Using Node
npx serve .
```

Then visit `http://localhost:8000` in your browser.

### Installing as an app
Once served over `http://localhost` or `https://`, most browsers will offer an **Install** / **Add to Home Screen** prompt — accept it to run Gree Runner as a standalone app with offline support.

## Project Structure

```
.
├── index.html       # Game markup, styles, and all game logic
├── manifest.json     # PWA manifest (name, icons, theme colors)
├── sw.js             # Service worker — caches assets for offline play
├── icon-192.png       # App icon (192x192)
└── icon-512.png       # App icon (512x512)
```

## Tech Stack

- **HTML5 / CSS3** — layout, theming via CSS custom properties, and animation
- **Vanilla JavaScript** — game loop driven by `requestAnimationFrame`, no frameworks or libraries
- **Web Audio API** — synthesized sound effects, no audio files
- **`localStorage`** — persists high score, selected theme, and sound preference
- **Service Worker + Web App Manifest** — offline caching and installability

## Customization

- **Themes**: edit the `THEMES` object in `index.html` to add or tweak color palettes.
- **Difficulty**: tune `GRAVITY`, `BASE_SPEED`, `MAX_EXTRA_SPEED`, and obstacle spawn logic near the top of the game script.
- **Icons / branding**: swap `icon-192.png` and `icon-512.png`, and update `manifest.json` accordingly.

## License

MIT — feel free to fork, modify, and use this project however you'd like.

---

Can you beat the high score?