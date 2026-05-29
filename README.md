# 🔓 Unlocked

**Open up, level up.** A 21-day hip-opening kickstart that scales into a year-long, milestone-gated mobility → strength → power program — built for staying athletic into your 50s and beyond (and, specifically, dominating the pickleball court).

**▶ Live app: https://zigrivers.github.io/unlocked/**

It's an installable, offline Progressive Web App. Add it to your iPhone home screen and it runs full-screen with no internet required (only the demo videos need a connection).

## Install on iPhone
1. Open the [live app](https://zigrivers.github.io/unlocked/) in **Safari**.
2. Tap **Share** → **Add to Home Screen** → **Add**.
3. Launch it from the new **Unlocked** icon — full-screen and offline-ready.

(Works on Android/desktop too via the browser's "Install app" option.)

## What it does
- **21-day kickstart**, then **12 blocks across 4 quarters**: Mobility Foundation → Strength-Through-Range → Power / Agility → Sport Integration.
- **Flexibility-led, milestone-gated:** you unlock each phase by hitting real benchmarks, not by the calendar.
- **Always-on prehab thread** (calf/Achilles + balance) from day one — the evidence-based defense against the injuries that sideline 50+ players.
- **Guided session player** with a timer, side switches, and form cues — plus a **review-first preview** of every session.
- **Hand-picked demo video** for each of ~60 drills.
- **Progress tracking:** streaks, a benchmark battery with charts, and a game-style level map.
- **Backup / restore** your progress as a file.

> ⚠️ Educational, not medical advice. Warm up, only ever feel mild tension (never sharp pain), and check with a clinician before starting — especially with any injury history.

## How it's built
A static, dependency-free web app:

| File | Purpose |
|------|---------|
| `index.html` | The entire app — vanilla HTML/CSS/JS, embedded fonts, all program content |
| `manifest.webmanifest` | PWA manifest (installable, standalone) |
| `sw.js` | Service worker — cache-first app shell for full offline use |
| `icons/`, `splash/` | App icon + iOS launch screens |
| `PROGRAM-BUILD-PROMPT.md`, `PWA-BUILD-PROMPT.md` | The specs this was built from |

No build step, no framework, no tracking. All progress is stored locally in your browser (`localStorage`).

## Run locally
```bash
# any static server works; e.g.
python3 -m http.server 8000
# then open http://localhost:8000
```
Or just open `index.html` directly (offline service worker only activates over http/https).

## Updating
Edit the files, bump the `CACHE` version in `sw.js`, then `git push`. GitHub Pages redeploys in ~1 minute, and the installed app shows a **"New version — Refresh"** prompt on next open.

---
🤖 Built with [Claude Code](https://claude.com/claude-code).
