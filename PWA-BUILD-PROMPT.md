# Build Prompt — "Unlocked" as an installable iPhone PWA (offline, home-screen icon)

> Decisions locked: PWA + Add-to-Home-Screen (no App Store); host free on GitHub Pages
> (public; no personal data in the file); must work fully offline after first load.

```
Turn "Unlocked" into an installable, offline, app-like experience on my iPhone: a real
home-screen icon that opens the app FULL-SCREEN (no Safari chrome) and works with no
internet. Do this as a PWA (Progressive Web App) + "Add to Home Screen", hosted free on
GitHub Pages. First THINK THROUGH and RESEARCH the current (2026) iOS realities, recommend
the approach, then implement it end to end and verify it.

CONTEXT
- The app is a single self-contained file: index.html in the git repo at
  ~/Developer/unlocked (branch main, already committed). It uses embedded fonts, localStorage
  for all progress/benchmarks, and external YouTube links for demos.
- Decisions already made: PWA + Add to Home Screen (no App Store); host on GitHub Pages
  (free, public — the program content is public, but no personal data lives in the file);
  must work FULLY OFFLINE after first load.
- Audience of one (me). Keep it simple, private-feeling, no analytics/tracking.

PHASE 1 — RESEARCH & THINK IT THROUGH (do this before coding; summarize findings briefly)
Research the current state (verify against 2026, iOS quirks change):
- iOS Safari PWA / Add-to-Home-Screen: what works and what doesn't today. Confirm there is
  no programmatic install prompt on iOS (unlike Android) and that A2HS is manual via the
  Share sheet — so I'll need exact tap-by-tap instructions.
- Standalone (full-screen) mode: required meta tags (apple-mobile-web-app-capable / the newer
  mobile-web-app-capable, apple-mobile-web-app-status-bar-style, apple-mobile-web-app-title),
  the web app manifest fields iOS actually respects vs ignores, theme-color, and
  viewport-fit=cover for the notch / Dynamic Island safe areas.
- Service workers on iOS Safari: support, scope rules, caching strategy for a tiny app shell,
  and the update lifecycle. Note a service worker must be a REAL separate file at the right
  path (cannot be inlined). Recommend the minimal file structure.
- Icons: exact sizes/formats iOS needs (apple-touch-icon 180x180 PNG, no transparency), plus
  manifest icons (192, 512, and a 512 "maskable" with safe padding). Assess iOS splash images.
- Offline DATA durability on iOS: the ~7-day eviction of unused PWA storage, Persistent
  Storage API on iOS, localStorage vs IndexedDB. Recommend a mitigation (Backup/Export & Import).
- The standalone "external link trap": tapping a normal link (YouTube demos) can strand me with
  no back button. Research the correct fix so demo links open in Safari / leave the app cleanly.
- iOS does NOT support the Vibration API in Safari — confirm and make haptics a graceful no-op.
- GitHub Pages specifics: enabling Pages, branch/folder, HTTPS, correct MIME for .webmanifest
  and sw.js, and cache-busting so updates propagate (cache versioning).
Briefly compare PWA-A2HS vs native wrapper (Capacitor) vs iOS Shortcut-to-URL; confirm
PWA-A2HS is right for one user, or flag if research changes that.

PHASE 2 — IMPLEMENT
Convert index.html into an installable, offline PWA while keeping ALL existing functionality
and visual design intact, and keeping it still openable as a plain local file (guard the
service-worker registration so a file:// open doesn't error):
- Web app manifest (name "Unlocked", standalone display, theme/background = app charcoal,
  relative paths so it works under the Pages subpath, icons, start_url, scope).
- Apple meta tags for full-screen standalone, status-bar style, app title; viewport-fit=cover;
  verify safe-area insets look right (notch + home bar).
- Design the "Unlocked" app ICON (lock/key mark, lime on charcoal, legible when small) as SVG,
  then generate PNGs (180 apple-touch-icon, 192, 512, 512 maskable with safe-zone padding).
- Service worker that caches the app shell for full offline use, versioned cache, clean update
  flow with an in-app "Update available - tap to refresh". Register only over http/https.
- Fix external (YouTube) links to open OUTSIDE the standalone app so I'm never trapped.
- Add Backup/Export and Import of my progress (localStorage) as JSON, in the menu.
- Native feel: momentum scroll, disable long-press callouts / double-tap zoom where right,
  clean tap targets and notch/home-bar safe areas in standalone.
- Vibration = graceful no-op on iOS; keep the sound cue.
Recommend and create the minimal file set (index.html, manifest.webmanifest, sw.js, /icons/*).

PHASE 3 — HOST ON GITHUB PAGES (end to end)
- Create the GitHub repo (gh), push, enable Pages, give me the live HTTPS URL. Confirm the
  manifest, service worker, and icons load over HTTPS and the app is installable + offline.

PHASE 4 — DELIVER & VERIFY
- Test SW registration + offline load, manifest validity, icon rendering, standalone detection,
  external-link behavior. Run a PWA/installability check if tooling allows. Report with evidence.
- Give tap-by-tap iPhone Add-to-Home-Screen instructions and how to verify offline.
- Explain how I push future updates and how they reach the installed app.
Commit and push everything. Only ask if truly blocking — otherwise make reasonable, well-
researched choices and ship it.
```
