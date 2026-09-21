# AGENTS.md

## Project overview
Static single-page PWA ("Mi Horario · Septiembre 2026"). No build step, no backend, no dependencies. All logic is inline in `index.html`; `sw.js` is a cache-first service worker; `manifest.json` + `icon-*.png` are PWA assets.

## Running
Served as static files via nginx (see `docker-compose.base44.yml`). No compilation or migrations needed. Edits to `index.html` / `sw.js` appear on reload — note the service worker caches aggressively, so hard-reload (or bump the `CACHE` name in `sw.js`) to see changes.

## Verification
`curl -s http://localhost:3000/` returns the `index.html` content; title is "Mi Horario · Septiembre 2026".
