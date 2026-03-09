# Focus Sprint — Performance Template v1

## Timebox
2 weeks (adjust as needed). This is a **focus lane**, not a rigid schedule.

## Objective (v1)
Ship a **10-minute performable set** built from Bitwig scenes triggered via Launchpad.

## Big shift / hypothesis (codified)
**Hypothesis:** Transition FX will feel more expressive and less repetitive if we switch from **pre-made, phase-synced automation curves** to **gesture-based control using an XY pad**.

- Current system: launch clip → automation curves sync to software phase → consistent but transitions start to “all sound the same.”
- Proposed system: XY pad gestures drive transition macro(s) in real time.

**XY semantics (codified):**
- **X = Drums transition amount** (one-knob style macro for the drums channel)
- **Y = Everything-else transition amount** (one-knob style macro for the “everything else” channel)
- On release: XY **bounces back to 0** (return/bounce speed is a tunable parameter in the template)

Success here is not guaranteed; the sprint is designed to **validate** this shift.

## Workplan (measurable)
### Phase 1 — Convert legacy transitions
- Convert the existing **16 transitions** into the new XY method:
  - 8 drums
  - 8 everything-else
- Evaluate: does it *feel* better to perform (expressiveness + less sameness)?

### Phase 2 — TouchOSC “assist” (phase-aware)
Goal: regain some of the old phase-locked reliability **without** losing gesture performance.

- Add two TouchOSC controls that temporarily take over the XY pad:
  - **Saw assist:** snap/drive XY into a saw-like ramp (recreates old curve vibe)
  - **Finish-at-end:** interpolate current XY position so it reaches **top/right** at the end of an **8-bar or 16-bar** phrase (configurable)

## “Getting somewhere” signals (pick 2–3)
- [ ] You can perform a continuous 10-minute run without stopping.
- [ ] You have at least 3 distinct transition “feels” (gesture-driven) that don’t collapse into the same sound.
- [ ] XY pad mapping is stable/repeatable enough that you *want* to practice it.
- [ ] BitwigTD → TouchDesigner → Resolume pipeline can reflect at least 2 useful parameters live (optional for v1).

## Constraints / guardrails
- Avoid overplanning. Keep notes to **next action** + blockers.
- Prefer small, testable experiments over large rewires.

## Next session (always keep this current)
- Next action:

## Blockers
- 

## Notes / discoveries (append)
- 
