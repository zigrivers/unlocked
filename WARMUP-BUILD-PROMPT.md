# Build Prompt — Illustrated, reusable exercise diagrams + instructions (starting with the warm-up)

> Locked decisions: rich REFERENCE (no timer for the warm-up); STATIC start→end pose diagrams
> with motion arrows, inline SVG, fully offline, on-brand; build it REUSABLE for all ~60 drills.

```
Upgrade the Pre-Pickleball Warm-Up in Unlocked (the index.html PWA at ~/Developer/unlocked,
repo github.com/zigrivers/unlocked, live on GitHub Pages) from a bare list into a rich,
illustrated reference. Build it as a REUSABLE illustration + instruction system that can later
be applied to every drill in the program — not a one-off for the warm-up. Think it through,
implement, verify, and ship.

LOCKED DECISIONS
- Rich REFERENCE (no timed walk-through for the warm-up — it stays a browseable sheet).
- Visuals = STATIC pose diagrams: a start pose and an end pose with motion arrows (PT-style),
  rendered as inline SVG, fully OFFLINE and on-brand (charcoal + lime). No external images.
- Build it REUSABLE so diagrams + instructions can be attached to any of the ~60 exercises.

APPROACH
- Build a PARAMETRIC SKELETAL-FIGURE renderer: one function that draws a simple human figure
  from joint angles (lean + per-leg thigh/shin/foot + per-arm upper/fore), so each exercise's
  diagram is DATA (start pose + end pose + arrows + view), not hand-drawn SVG. A `view`
  flag (side vs front) controls limb fading/spread. Allow custom poses for floor/seated shapes.
- Extend the data model with structured INSTRUCTIONS per exercise — ordered steps
  (Setup → Execute → Key cue → Common mistake/safety) — and a DIAGRAM spec (start, end, arrows,
  view). Keep existing cue/feel/regression/video fields; this augments them. Store it so it's
  reusable across the warm-up sheet, the session preview, and (optionally) the player.

IMPLEMENT
- The figure renderer + a library of POSE PRESETS covering the needed positions. Render a
  diagram as start→end (side-by-side small figures with a motion arrow between; ghost/dim start,
  bright-lime end). Crisp on a phone, accessible (aria-label describing the movement).
- Rebuild the Pre-Pickleball Warm-Up sheet as a rich reference: for EACH move show the diagram,
  reps/time, step-by-step instructions, the "feel it / not" note, a safety line, and the
  existing "watch demo" video link. Keep the honest framing up top. Validate/curate the 7 moves
  against good warm-up practice (raise temp → mobilize → activate → prime fast movement).
- Surface the same diagram + steps inside the existing session PREVIEW for any drill that has
  them, with GRACEFUL FALLBACK (cue + video as today) for drills not yet authored. Don't break
  anything that works now.

COVERAGE (be honest — no silent gaps)
- Fully author diagrams + step instructions for all 7 warm-up moves now.
- Author as many remaining drills as feasible this pass, prioritizing the highest-value standing
  movements (deep squat, goblet squat, RDL, split squat, calf eccentrics, lunges, hip CARs…).
- Document the PATTERN for adding the rest and output a COVERAGE LIST: which drills have a
  diagram + steps vs which still fall back to cue+video. Don't imply full coverage if absent.

VERIFY & SHIP
- Test in a browser: warm-up reference renders with legible diagrams + steps on phone width; the
  session preview shows diagrams where authored and falls back cleanly where not; no regressions.
  Show evidence. Keep it fully offline (inline SVG only). Bump the service-worker CACHE version.
- Commit and push; confirm GitHub Pages redeploys live; note the in-app "Refresh" picks it up.
Make reasonable choices and ship it; only ask if truly blocking.
```
