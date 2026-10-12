# Atelier Riviera

A private personal wardrobe app: a closet, an outfit generator with strict colour rules, a wear journal, uniforms, gap analysis, a buy checker and a packing planner. One file, no build step, made for a phone.

## Privacy

- This repository contains **code only**. No closet, favourites, history or settings are stored here.
- All personal data lives in the browser's local storage on the device, and optionally in a **separate private repository** as a single `data.json` backup, written with a fine-grained token that the user pastes into the app. The token is kept in local storage only.
- The page can only talk to two hosts, enforced by its Content-Security-Policy: Open-Meteo for the weather and the GitHub API for the backup. No analytics, no tracking, `noindex`, `robots.txt` disallows everything.

## Files

- `index.html`: the whole app (inline CSS and JS, fonts embedded).
- `sw.js`: service worker so the app opens offline after the first load.
- `manifest.webmanifest`, `icon-*.png`: home-screen install.
- `.github/workflows/pages.yml`: deploys the folder to GitHub Pages on every push to `main`.

## Restore on a new device

Open the app, go to Settings, paste the token, tap Restore.
