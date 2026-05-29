# Build Prompt — Deep multi-agent accuracy audit of the exercise diagrams

> Locked decisions: audit + fix + ship; deep multi-agent (independent reviewer per exercise +
> adversarial verify), cross-checked against each drill's demo video and known biomechanics.

```
Audit EVERY illustrated exercise diagram in Unlocked for movement accuracy, fix the ones that
are wrong, re-verify, and ship. Use a DEEP MULTI-AGENT approach: fan out independent reviewers,
one per exercise, cross-check each against its real demo video and known biomechanics, run an
adversarial "is this actually correct?" pass, then apply and visually verify the fixes.

WHERE THINGS LIVE (index.html in ~/Developer/unlocked, repo github.com/zigrivers/unlocked):
- DOC = { id: {view:'side'|'front', start, end, arrows:[svgPaths], steps:[{k,v}], aria} } — 64
  entries (all 61 EX library drills + 3 warm-up-only ids: march, bwsquat, calfraise).
- A pose = {lean, legs:[{t,s,f},{t,s,f}], arms:[{u,e},{u,e}]}. Angles are DEGREES measured from
  straight-DOWN, increasing toward the FRONT (+x): 0=down, 90=forward/right, 180=up, -90/270=back.
  legs[0]/arms[0] = the FAR limb (dimmed in side view). `lean` tilts the torso (+ leans forward;
  in front-view it reads as a lateral lean). t=thigh, s=shin, f=foot; u=upper arm, e=forearm.
- diagramSVG(DOC[id]) renders the start (dim) + finish (bright) figures with a motion arrow.
- EX[id] holds the ground-truth cue (.c), feel (.f), regression/progression, and the verified
  YouTube demo URL (.v). DOC[id].steps holds the written instructions.

GROUND TRUTH for "accurate" (per exercise):
1. The real movement's key checkpoints — the correct joint positions at START and FINISH.
2. The exercise's own cue text (EX[id].c/.f) and steps — the figure must match them.
3. The hand-picked demo video (EX[id].v) — the canonical reference for the positions.
The BAR: the diagram must correctly convey the key start/finish positions AND the direction of
movement. It's a simple 2D stick figure — judge whether it's biomechanically RIGHT and READABLE,
not photorealistic. Be especially critical of: squat/hinge depth and shin angle, which way the
torso leans, front-vs-side view choice, lifted-vs-planted limbs, and the supine/side-lying poses
(glutebridge, hipthrust, deadbug, hamstrap, sideplank, copenhagen, openbook).

METHOD (deep multi-agent):
- Phase 0 (orchestrator): render a PNG of all 64 diagrams and view them as a visual baseline.
- Phase 1 REVIEW (one agent per exercise): give each agent the name, cue, demo-video URL, the
  angle convention, and the ACTUAL start/end angles. It states the correct checkpoints in this
  convention, compares, returns a verdict (ACCURATE / MINOR / NEEDS-REWORK) + concrete corrected
  angles if needed.
- Phase 2 ADVERSARIAL VERIFY (second agent): tries to refute the verdict and validates that the
  proposed angles produce a correct, readable, in-frame pose with a matching arrow. Only apply a
  change when it's clearly a net improvement.
- Phase 3 APPLY & VISUALLY VERIFY (orchestrator): apply confirmed fixes, re-render the changed
  diagrams, and visually confirm they look better; iterate or revert if not. If the renderer
  genuinely can't express a movement, say so and either improve the renderer or accept with a note.

DELIVERABLES: a verdict table for all 64 (id, verdict, what was wrong, old→new); the applied fixes,
visually re-verified with evidence; an honest summary; bump the service-worker cache, commit, push,
and confirm GitHub Pages redeployed live. Make well-verified changes and ship; ask only if blocking.
```
