# Bible & continuity

Merged from the mini-dramas Character Bible, the documentary's period-accuracy rules and
the stickman agent's continuity system — restated for business documentaries.

## Build order
1. **Founder master image first.** Standalone, approved, saved. It is the Consistent
   Character reference for every clip with that person — including clip 1. Scene images
   never become the master.
2. **Location masters** for every recurring place (HQ, store, factory floor): fixed
   layout — landmarks, neighbours, distances, camera side — written into a block and
   reused verbatim. Reject mirrored/swapped sets on sight.
3. **Era audit** per location block: year pinned; tech, vehicles, clothing, signage style
   all of that year. One anachronism fails the clip.

## Continuity planning (before generating anything)
Design the whole sequence as a table: for each clip — **incoming state** (where people/
props are, what just happened) → **action** → **outgoing state** → **next clip's opening**.
Submit in that order; prepare the next start image while earlier clips render.
Don't restart the same approach/reach from a neutral pose in consecutive clips — Auto
Align fixes gaps, not repeated action.

## Start-image sourcing
Default: **fresh start image** generated from the master(s) + the planned incoming state.
Last-frame chaining only when the next clip opens at the *same framing* — chaining
compounds drift (faces, outfits, props quietly mutate), and a closer framing redraws
detail from text.

## Drift control
- Bible blocks pasted verbatim; a better frame updates the bible once, centrally.
- Stable identities and **counts**: "one plant", "three partners", "two stores" — counts
  are checked in every start image before animating.
- Eyelines: people in conversation face each other (side-on / three-quarter), never
  stare into the lens; the master preserves identity, not a front-facing pose.
- Keep usable clips despite minor gaze/camera differences; reserve re-rolls for identity,
  era, count or layout failures.
