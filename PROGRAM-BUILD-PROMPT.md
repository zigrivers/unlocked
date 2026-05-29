# Build Prompt — "Unlocked" (Year-Plus Periodized Mobility + Strength Program, Web App)

> Paste everything in the code block below back to Claude to build the app. It is the
> finalized, research-grounded build spec. Design decisions locked: flexibility-led +
> milestone-gated + always-on prehab; 21-day kickstart on-ramp; 12 blocks / 4 quarters
> authored as repeatable weekly templates; strict 15-min/day with optional longer-session
> accelerators flagged (never required); home-gym weights used on strength days;
> injury-prevention weighted to 50+ pickleball danger zones.

```
Build me a YEAR-PLUS, milestone-based periodized MOBILITY + STRENGTH + ATHLETIC program,
delivered as a single-file, offline-capable interactive web app (one self-contained .html
file: inline CSS + JS, no build step, no external runtime dependencies; opens by
double-clicking; works great on phone and desktop). The 21-day hip-opening program is the
ON-RAMP (Phase 0) to a 12-block, four-quarter annual arc.

BRANDING: The program is named "Unlocked" (tagline: "open up, level up"). Lean into the
unlock metaphor throughout the UI — phases/blocks are LOCKED until I hit the milestone gate
that UNLOCKS them, and clearing a gate should feel like a satisfying "unlock" moment. Use the
name in the app title, home screen, and program map.

=========================================================
WHO IT'S FOR
=========================================================
- A healthy ~56-year-old man, beginner/stiff, desk-bound, with a HOME GYM (adjustable
  dumbbells/kettlebells/barbell-class access).
- North-star goal: be an exceptionally athletic 56-year-old PICKLEBALL player — mobility,
  single-leg & rotational strength, age-appropriate power, lateral agility, and durability.
- TIME BUDGET IS FIXED: ~15 minutes per day, EVERY day. All strength/power/agility work must
  fit INSIDE the rotating daily 15 minutes — do NOT design separate long sessions as required.
  Where a longer optional weekend session would meaningfully accelerate a specific milestone,
  SAY SO as an optional add-on and let me decide; never make it mandatory.
- Equipment: design so every routine works with minimal equipment (floor + wall), but USE the
  home-gym weights on strength days. Always give a no-equipment regression and a harder
  progression for each drill. Optional props: yoga block, strap, cushion, sturdy box/step.

=========================================================
GOVERNING PHILOSOPHY — FLEXIBILITY-LED, MILESTONE-GATED, PREHAB ALWAYS-ON
=========================================================
- FLEXIBILITY LEADS but is never the ONLY thing. Q1 is ~70-80% mobility; later phases are
  UNLOCKED BY HITTING CONCRETE MILESTONES (achievement-gated), not by the calendar. If a gate
  isn't met, the app keeps me in the current phase with extra mobility focus rather than
  pushing me forward.
- New range must be OWNED: pair passive stretching with active/loaded end-range work
  (CARs, PAILs/RAILs end-range isometrics, loaded mobility) so range becomes usable & retained.
- ALWAYS-ON PREHAB THREAD from Day 1, regardless of phase (this is non-negotiable and
  evidence-driven for a 50+ pickleball player):
    * Eccentric / heavy-slow CALF-ACHILLES loading. Progress toward the Alfredson protocol
      (straight-knee + bent-knee heel drops, building to 3x15 each, ~3-sec lowering, loaded
      with a backpack) and/or Heavy Slow Resistance calf work (3-sec up / 3-sec down). This is
      the #1 protector against the Achilles ruptures/tendinopathy that dominate 50+ pickleball
      injuries (68% of those ruptures happen in the player's first month of play).
    * Single-leg BALANCE / proprioception (eyes-open -> eyes-closed -> unstable progression).
    * A graded WARM-UP routine to do BEFORE any pickleball play (most acute injuries happen
      cold, on sudden push-off / direction change).

=========================================================
HONEST EXPECTATIONS (build these into an intro screen + per-block framing)
=========================================================
- Phased physiology: Weeks 1-4 = mostly NEURAL gains (stretch tolerance + access to existing
  range), fast and motivating. ~8-12+ weeks = slower connective-tissue/architectural change
  ("earned-inch" phase). Months-to-years = deep structural/collagen remodeling. Front-load
  rapid-progress messaging in Q1; reframe mid-year as consolidation + strength-through-range.
- 21 days launches a STREAK, not an automatic habit (true automaticity averages ~66 days, range
  18-254). Build "missed a day? streaks bend, they don't break" messaging; never all-or-nothing.
- Milestones are LIKELY-FOR-MANY RANGES, not guarantees — progress varies hugely by individual.
  Define "progress" broadly (longer holds, more comfort, less soreness count too).
- Do NOT promise full middle splits — hip bony anatomy can hard-cap it. Mark deep-split goals
  as optional/individual.

=========================================================
PHASE 0 — 21-DAY KICKSTART (full day-by-day detail)
=========================================================
Author all 21 days in full daily detail (this is the habit on-ramp and hip foundation):
- Beginner-friendly, ~15 min, mostly gentle static holds + hip CARs, with the prehab thread
  woven in from Day 1 (short calf eccentric set + balance).
- Session skeleton: ~3 min dynamic warm-up + hip CARs -> ~9-10 min of 2-4 targeted holds
  (30-60 sec x 2) -> ~2 min of one active/loaded "own-the-range" element (PNF contract-relax
  ~5s contract->20-30s deeper stretch, or a 90/90 lift-off).
- Cover all six hip directions across the 3 weeks, prioritizing desk-sitter deficits: hip-flexor
  length / hip extension, INTERNAL rotation (most overlooked), external rotation/glutes,
  adduction/groin, hamstrings, integrated deep squat; include an ankle-dorsiflexion drill.
- High-ROI recurring anchors: 90/90 (+ active lift-offs), couch stretch, deep squat/malasana,
  frog OR cossack, pigeon/figure-4, hip CARs.
- Week 1 establish/tolerance; Week 2 add depth + PNF/end-range isometrics; Week 3 add light
  loaded/active end-range + DAY-21 RE-TEST.
- "What to expect after 21 days" screen that transitions into Phase 1.

=========================================================
THE ANNUAL ARC — 12 BLOCKS / 4 QUARTERS
=========================================================
Author each block as a COMPLETE REPEATABLE WEEKLY TEMPLATE (7 daily 15-min sessions) plus
progression notes for build-weeks 1-3 and a Week-4 DELOAD + RE-TEST. (Don't hand-author 365
unique days — periodization works in repeating blocks.) Each block = 3 build weeks + 1 deload/
re-test week. Each block specifies: theme, the 7-day rotating template, what progresses across
the 3 build weeks, the deload protocol, the RE-TEST measures, and the MILESTONE GATE to advance.

The daily 15 min ROTATES discipline by day-of-week and EVOLVES by quarter. Respect masters
recovery: >=48h (up to 72h) between hard sessions, deload every 4th week, autoregulate with RIR
(stop 2-3 reps shy of failure). Example weekly shape (adjust per quarter):
  Mon strength(lower) - Tue mobility/floor - Wed strength(upper+rotational)/prehab -
  Thu mobility/floor - Fri power-agility (later quarters)/strength - Sat optional-longer or play -
  Sun easy mobility + balance + recovery. Calf-eccentric + balance threaded into most days.

--- Q1 — MOBILITY FOUNDATION (neural-gain phase; ~70-80% mobility) ---
  Block 1 — Squat & Ankle Base: daily deep-squat accumulation + ankle DF + intro calf loading.
     Milestone: relaxed flat-foot deep-squat hold ~30-60s; less bottom-of-squat discomfort.
  Block 2 — Hip Floor Sitting: 90/90 + pigeon focus.
     Milestone: shift side-to-side in 90/90 without hands; comfortable upright cross-legged sit.
  Block 3 — Posterior Chain & Couch Stretch: hip-flexor/quad length + early pancake reach.
     Milestone: visibly deeper couch stretch; longer comfortable floor-sitting.
  GATE TO Q2: flat-foot deep-squat hold >=60s; controlled 90/90 both sides w/o hands;
     cross-legged sit >=2 min comfortably.

--- Q2 — STRENGTH-THROUGH-RANGE (tissue + load phase) ---
  Block 4 — Loaded Mobility Intro: CARs progressions + PAILs/RAILs end-range isometrics; begin
     closing the active-vs-passive ROM gap.
  Block 5 — Foundational Strength: 2-3x/wk squat/hinge/lunge/carry, 1-4 sets x 8-15, RIR 2-3;
     establish HSR/Alfredson calf work. Milestone: ~10-20% load increases (relative beginner).
  Block 6 — Single-Leg & Tendon: split squats, step-ups, heavy-slow calf. Milestone: improved
     single-leg balance/strength symmetry; calf endurance up. (Set expectation: tendon stiffness
     gains need ~8-12 wks heavy load.)
  GATE TO Q3: single-leg balance >=30s/side eyes open; full-ROM controlled bodyweight split
     squat; ~20 single-leg calf raises/side; 4+ wks pain-free 2x/wk strength; pain-free landing
     from a sub-max jump.

--- Q3 — POWER / AGILITY (Type-II + elastic phase; follows a strength base) ---
  Block 7 — Power Intro: age-adapted plyo ramp (start with 2x15-20 NO-jump patterning -> sub-max
     hops), med-ball throws. Milestone: pain-free landing/jump mechanics.
  Block 8 — Plyo + Change-of-Direction: maximal jumps 3-4x6-8, lateral shuffles, and explicitly
     BACKWARD COD + deceleration drills (most falls happen lunging or moving backward). Progress
     conservatively — watch calf/gastroc strain. Milestone: jump height/power up (~7-17% over
     ~12 wks typical); faster COD.
  Block 9 — Reactive / Lateral Agility: split-step reactions, multidirectional lunging under
     light fatigue, hip-abductor strength (separates pickleball players). Milestone: faster,
     more controlled directional change.
  GATE TO Q4: pain-free controlled landings + lateral shuffle + backward COD; demonstrable
     rotational core capacity.

--- Q4 — SPORT INTEGRATION (undulating maintenance while playing) ---
  Block 10 — On-Court Conditioning: integrate movement + skills; maintain strength/power.
  Block 11 — Rotational Power & Overhead Prep: rotational core, serve/smash prep, + shoulder
     rotator-cuff and forearm/grip prehab ("pickleball elbow"). Milestone: more drive/serve power
     without shoulder/elbow flare.
  Block 12 — Peak / Taper & Annual Re-Test: reduce volume, keep playing, re-test EVERYTHING.
  ANNUAL TARGETS (honest): durable deep squat + floor sitting; closed active/passive ROM gap in
  hips/ankles; meaningfully stronger single-leg + calf/Achilles resilience; measurable jump/COD
  power gains; pickleball-ready agility. Deep splits = optional/individual.

=========================================================
EACH DAILY SESSION MUST INCLUDE
=========================================================
- Block, week (build 1-3 or deload), day theme, and "today's discipline" (mobility / strength /
  power-agility / prehab-recovery).
- Ordered drills with: name, target, exact duration or sets x reps, per-side note, load guidance
  (RIR cue on strength days), 1-2 plain-language form cues, a "feel it here / NOT here" note,
  and the regression + progression.
- A built-in guided TIMER that auto-advances through the drills (work intervals, side-switch
  and rest prompts), with audible + visual cues and pause/skip/back, landing at ~15 min.
- Relevant safety reminder; on strength/power days, the prescribed rest between sets.

=========================================================
SELF-ASSESSMENT, GATES & PROGRESS TRACKING
=========================================================
- Benchmark battery captured at Day 1, Day 11, Day 21, and every block boundary (Week-4 re-test).
  Grow the battery by phase:
    Mobility: deep-squat hold quality/time, sit-and-reach, 90/90 rotation symmetry, couch-stretch
      depth (torso angle), cross-legged comfort (1-10), ankle dorsiflexion (knee-to-wall cm).
    Strength/Power (added Q2+): single-leg balance time, single-leg calf-raise reps, split-squat
      quality, a key lift load, and (Q3+) a vertical/broad jump proxy + a simple COD/agility time.
- MILESTONE GATES gate phase progression: show me my current gate, my measured status, and
  whether I've met it. If not met, recommend staying/repeating with targeted focus rather than
  advancing. Let me override if I choose.
- Daily completion checkboxes + visible STREAK counter + block/quarter progress bar. Persist
  EVERYTHING in localStorage (no account, no server). Let me jump to any day/block; don't lock me
  out. Show before/after comparisons and simple progress CHARTS over time.

=========================================================
VIDEO LINKS
=========================================================
- For each distinct drill, link a specific free YouTube demonstration (prefer GMB, Tom Merrick /
  Bodyweight Warrior, The Ready State, Yoga With Adriene, and physical therapists; for the calf
  protocol, a clear Alfredson/HSR demo). Open in a new tab. If unsure a specific URL is live, link
  a YouTube SEARCH query for the exact drill name and label it as a search link rather than
  guessing a video ID. Collect all sources in a References section.

=========================================================
SAFETY (50+ specific)
=========================================================
- Warm up first; only tension/mild discomfort, never sharp pain. Go easy on deep knee-flexion
  holds (pigeon, couch, hero) if knees object — use cushion regressions.
- Heavy strength & plyometrics follow a base, ramp conservatively, and need >=48h spacing; plyo
  carries real strain risk (esp. calf) — patterning before intensity.
- Always do the graded warm-up before pickleball play. Flag caution for hip impingement,
  hypermobility, acute injury. Encourage post-session protein and sleep as part of recovery.

=========================================================
UI / UX & DELIVERY
=========================================================
- Calm, mobile-first, big tap targets, readable mid-workout, dark-mode friendly.
- Screens: Home/dashboard (streak, today's session, current block + gate status, jump-to), the
  daily session player with timer, the benchmarks/progress screen with charts, and a program-map
  overview (Phase 0 -> 12 blocks -> annual targets).
- Pure vanilla HTML/CSS/JS in ONE file; inline any library you use; use inline SVG or emoji for
  pose icons, not external images.
- Deliverables: the single .html file, a brief how-to-use note, and a list of any drills/video
  links you were unsure about. Make reasonable, evidence-based choices and BUILD IT — only ask me
  if something is truly blocking.
```
