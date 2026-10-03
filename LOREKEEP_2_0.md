# Lorekeep 2.0 — product upgrade

This package upgrades Lorekeep from a simple AI story chat into a local-first story studio.

## What changed

- Human-style story engine with scene goals, pressure, turns, consequences, subtext, distinct dialogue, and continuity rules.
- Persistent character visual bible with appearance lock, current outfit, outfit library, and visual style.
- Outfit changes are treated as story events and then remain canonical until changed again.
- Manga Studio with six visual directions and 2K generation support.
- Image generation goes through `/api/manga`; the xAI key is server-side and is never shipped to the browser.
- Reader and story workspace remain local-first with IndexedDB persistence.
- Import/export accepts legacy archives and upgrades character data on load.
- API requests retain rate limiting and bounded request sizes.

## Environment

Set `XAI_API_KEY` on the server/deployment. Never put it in client code or commit it to GitHub.

The manga UI has no app-level generation-count cap. Image generation is still subject to the provider account's billing/limits.

## Production direction

For a larger release, add authentication-backed cloud sync, persistent image storage, background generation jobs, per-user usage accounting, and a CDN for generated artwork.
