# Exercise Diagram Accuracy Audit

Deep multi-agent audit of all 64 illustrated exercises: an independent reviewer rated each diagram's start/finish joint angles against the movement's real biomechanics and its demo video, then an adversarial verifier confirmed or rejected each proposed fix. Confirmed fixes were applied and visually re-verified.

- Reviewer flagged: 22 MINOR, 40 NEEDS_REWORK, 2 ACCURATE
- After adversarial verification: **54 fixes applied**, 10 left as-is (original confirmed correct or proposed fix rejected).

| Exercise | Reviewer | Final | Changed | Key issue addressed |
|---|---|---|---|---|
| adductorrock | NEEDS_REWORK | MINOR | ✅ fixed | View is wrong: the defining feature of this exercise is one leg extended OUT TO THE SIDE (lateral abduction) p |
| ankledorsi | MINOR | MINOR | — | Correct elements: side view is right; the NEAR (front) leg is the working/planted leg and it correctly rocks t |
| backpedal | NEEDS_REWORK | MINOR | ✅ fixed | FINISH lean=-6 leans the torso BACKWARD, which directly contradicts the key coaching cue 'Avoid leaning too fa |
| bandpull | NEEDS_REWORK | MINOR | ✅ fixed | FINISH arm angles flip sign to negative (u:-94/94, e:-96/96 ~ horizontal but in the BACKWARD/rear hemisphere g |
| boxjump | NEEDS_REWORK | MINOR | ✅ fixed | FINISH misrepresents the position. The cue is 'jump up, land softly on the box, STAND TALL' but the current fi |
| broadjump | NEEDS_REWORK | MINOR | ✅ fixed | FINISH misrepresents a 'soft landing': legs are nearly straight (t:40/28, s:-10/-6), which reads as the stiff/ |
| bulgarian | NEEDS_REWORK | ACCURATE | ✅ fixed | DEPTH: The front (working) leg barely descends. Front knee interior angle goes from ~166 deg (START) to only ~ |
| butterfly | NEEDS_REWORK | MINOR | — | View/motion mismatch: the diagram is a FRONT view, but the only real movement in a butterfly stretch is a forw |
| bwsquat | NEEDS_REWORK | MINOR | — | FINISH shin angle is backward: s=-18 tilts the shin behind the knee, which pushes the knee back over the heel  |
| calfbent | MINOR | MINOR | ✅ fixed | FINISH feet are asymmetric (near foot f=78 vs far foot f=96). On a two-leg heel raise both feet press up toget |
| calfecc | NEEDS_REWORK | MINOR | ✅ fixed | Single-leg movement not depicted: both legs are nearly identical and planted. An eccentric single-leg heel dro |
| calfraise | NEEDS_REWORK | ACCURATE | ✅ fixed | Foot-angle direction misrepresents the lead action. f goes 100->138 on BOTH feet, which is dorsiflexion (toes  |
| carry | NEEDS_REWORK | ACCURATE | ✅ fixed | FINISH lean=4 introduces a lateral lean toward the loaded side. In front view this reads as the figure tipping |
| catcow | NEEDS_REWORK | ACCURATE | ✅ fixed | Shin angle s=-150 lifts the shins/feet off the floor (ankle rises to y≈3 vs knee y≈24); in true all-fours the  |
| copenhagen | NEEDS_REWORK | ACCURATE | ✅ fixed | Body orientation is wrong: a Copenhagen plank is a near-horizontal SIDE plank, but the current pose (lean 40,  |
| cossack | NEEDS_REWORK | MINOR | ✅ fixed | Lean direction is wrong relative to the working leg. The torso leans +16 toward the NEAR (+x) leg, but the dee |
| couch | MINOR | MINOR | ✅ fixed | Back knee floats ~17 units above the floor/front-foot line; in a couch stretch the back knee rests (padded) on |
| couchpails | MINOR | MINOR | ✅ fixed | The static pose is anatomically correct (rear leg fully flexed with shin up against couch, front leg planted l |
| dbrow | ACCURATE | ACCURATE | — | Braced/FAR arm hangs straight down (u=8) identical to the working arm rather than reaching forward to a bench  |
| deadbug | NEEDS_REWORK | ACCURATE | ✅ fixed | View is correct (side), but the pose does not read as lying on the back in a Dead Bug. The arms (u:60,e:60) po |
| decel | NEEDS_REWORK | MINOR | ✅ fixed | FINISH knees are nearly straight (shin s=-12 and -14, essentially extended) — fails to show the low, knee-soft |
| deepsquat | NEEDS_REWORK | MINOR | ✅ fixed | DEPTH: Current FINISH thigh t=58 with shin s=-22 places the knee BELOW the hip (knee y=+12.7 vs hip y=0). That |
| extrot | MINOR | MINOR | — | The exercising (working) arm is the NEAR arm conceptually, but the diagram puts the moving arm on the FAR side |
| frog | NEEDS_REWORK | MINOR | ✅ fixed | Shin angle s=-150 points the lower legs steeply UP/back, lifting the shins off the floor. In a true quadruped  |
| glutebridge | NEEDS_REWORK | ACCURATE | ✅ fixed | Legs are inverted: with t=60/s=170 the knee lands BELOW the hip (y=-12) while the ankle/foot float ABOVE it (y |
| goblet | NEEDS_REWORK | ACCURATE | ✅ fixed | FINISH depth far too shallow: thigh angle t=52 leaves the hip well above the knee (a quarter squat). A goblet  |
| halfkneel | NEEDS_REWORK | ACCURATE | ✅ fixed | Rear/down shin angle (s=-150 start, -150 finish) is anatomically wrong: it sends the rear ankle/foot UP and ba |
| hamstrap | MINOR | MINOR | ✅ fixed | START raised leg is already near-horizontal (t=s=96); the lift range to FINISH (120) is only ~24 deg, so the m |
| hipairplane | NEEDS_REWORK | NEEDS_REWORK | — | View cannot show the movement: the defining action is the pelvis rotating OPEN toward the ceiling (hip IR/ER a |
| hipcars | MINOR | MINOR | ✅ fixed | CORRECT key positions (this convention): standing leg straight down (t~0,s~0,foot planted). START = hip flexio |
| hipcircle | NEEDS_REWORK | ACCURATE | ✅ fixed | Hands are on the hips and must stay FIXED, but the arms change between START ({-28,-40}/{28,40}) and FINISH ({ |
| hipthrust | NEEDS_REWORK | ACCURATE | ✅ fixed | Shins point nearly straight up (s=168 in both poses), placing the ankle ABOVE the knee. This depicts feet in t |
| hsrcalf | MINOR | MINOR | ✅ fixed | START foot angle f=100 reads as a flat/neutral foot, not the heel-dropped (dorsiflexed) bottom position you ge |
| inchworm | NEEDS_REWORK | ACCURATE | ✅ fixed | FINISH legs are wrong for a plank: thighs/shins are nearly straight DOWN (t around 4/-4, s around 2/-2). With  |
| jumppattern | NEEDS_REWORK | MINOR | ✅ fixed | FINISH shin angle is the wrong direction: current shin = -14 makes the lower leg kick backward (knee forward,  |
| lateral_lunge | MINOR | MINOR | ✅ fixed | Bent-knee depth is shallow: FINISH NEAR thigh t=30 reads more like a shallow shift than a true sit-back lunge; |
| legswing | MINOR | MINOR | ✅ fixed | Planted-foot angle is slightly over-plantarflexed (f:100); a flat stance foot reads cleaner at ~92-95 in this  |
| lizard | MINOR | MINOR | — | Direction and view are correct (side view, forward lean, front leg deeply flexed, back leg long). The movement |
| march | MINOR | MINOR | ✅ fixed | Lifted-leg shape is wrong for a knee drive. Current lifted leg (t:60, s:120, f:118) places the knee BELOW hip  |
| mbrot | NEEDS_REWORK | NEEDS_REWORK | ✅ fixed | View is FRONT, but a rotational med-ball throw is a transverse-plane movement that a front view cannot depict: |
| mbslam | MINOR | MINOR | ✅ fixed | FINISH thighs at t=30 swing FORWARD, which reads as a deep forward bend/partial squat rather than a true hip h |
| ninety | MINOR | MINOR | — | Leg geometry does not clearly read as a seated 90/90: the front (NEAR) thigh 96 / shin 150 and back (FAR) thig |
| ninetylift | NEEDS_REWORK | MINOR | ✅ fixed | Wrong plane/view: 90/90 lift-offs are a transverse-plane (hip rotation) exercise. In a pure SIDE view the two  |
| ninetypails | MINOR | MINOR | — | The deepening fold (lean 30 to 38, only 8 degrees) is correct in direction but subtle; it reads as almost no c |
| ohp | MINOR | MINOR | ✅ fixed | START rack reads as flared forearms: the near forearm e=118 sits ~28 deg from horizontal, so the hands swing O |
| openbook | ACCURATE | ACCURATE | — | None significant. Optional polish: the finish near-arm forearm could carry a slight elbow bend for a more natu |
| pallof | NEEDS_REWORK | MINOR | ✅ fixed | Arms point in opposite horizontal directions (NEAR upper-arm u=-60 points down-and-back, FAR u=60 points down- |
| pancake | NEEDS_REWORK | MINOR | ✅ fixed | FINISH uses lean=46 to depict the forward fold, but in a FRONT view 'lean' reads as a sideways/lateral tilt, n |
| pigeon | NEEDS_REWORK | MINOR | ✅ fixed | Front (folded) leg is not represented: NEAR-leg thigh t=-66 points up-and-back, so both legs effectively point |
| pogo | NEEDS_REWORK | ACCURATE | ✅ fixed | Foot-angle direction is reversed: f goes 100 to 135 (toward toes-up/dorsiflexion), but a pogo hop is plantarfl |
| rdl | MINOR | MINOR | ✅ fixed | FINISH hinge depth is slightly shallow at lean 64; a true RDL bottom has the flat back closer to parallel (~70 |
| seatedfold | MINOR | MINOR | ✅ fixed | Finish fold depth is a bit shallow: lean=54 reads as a half hinge. A seated forward fold toward the feet folds |
| serveprep | MINOR | MINOR | ✅ fixed | Readability: the arm that performs the full overhead reach is the FAR limb (index 0), which is drawn faded in  |
| shortfoot | NEEDS_REWORK | MINOR | ✅ fixed | START and FINISH poses are byte-for-byte identical, so the diagram shows no movement at all — the arch-lift ac |
| shuffle | NEEDS_REWORK | ACCURATE | ✅ fixed | Depth/knee-bend missing: in both poses the shins nearly continue the thigh line (START FAR t-20/s-10, NEAR t20 |
| sideplank | NEEDS_REWORK | MINOR | ✅ fixed | View is wrong: a side plank should be drawn FRONT view so the straight diagonal body line, stacked hips, plant |
| skater | MINOR | MINOR | ✅ fixed | Landing leg shows no knee bend: the core cue is 'land soft on a bent knee,' but in the FINISH the planted/land |
| slbalance | MINOR | MINOR | ✅ fixed | FINISH torso lean=4: cue says 'tall posture, stay still and quiet' — a lateral lean in front view reads as los |
| splitsquat | NEEDS_REWORK | MINOR | ✅ fixed | FINISH front knee barely bends (front leg s=-6 keeps the shin nearly collinear with the thigh, knee almost str |
| splitstep | NEEDS_REWORK | MINOR | ✅ fixed | FINISH does not lower: shins stay nearly in-line with thighs (s only +-10), so the figure spreads its feet but |
| stepup | NEEDS_REWORK | ACCURATE | ✅ fixed | START top leg (box foot) is not properly folded: shin s=-10 leaves the knee almost straight, so the raised leg |
| tibraise | MINOR | ACCURATE | ✅ fixed | START foot angle f=100 is slightly plantarflexed (toes pointing down past horizontal). A tibialis raise should |
| worldsgreat | NEEDS_REWORK | MINOR | ✅ fixed | Front lunge leg lacks knee bend: the FAR leg has shin s:0 (a straight leg angled forward), so the figure does  |
| wristcurl | NEEDS_REWORK | MINOR | ✅ fixed | Figure is standing, not seated: thighs and shins both hang nearly straight down (t:4/s:3 and t:-4/s:-3 ~= vert |
