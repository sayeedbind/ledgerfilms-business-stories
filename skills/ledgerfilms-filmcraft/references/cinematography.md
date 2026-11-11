# Cinematography — camera language for AI video prompts

Every prompt is a camera instruction. Vague prompts (“cinematic scene of a market”) produce slideshow stills; precise camera language produces film.

## Shot sizes (name one in every prompt)
- **ECU** extreme close-up — a detail carries the meaning (a key turning, a counter digit, a hand stopping mid-air).
- **CU** close-up — face/hands/object; emotion and decisions.
- **MS** medium shot — waist-up character in a place; the workhorse for actions.
- **WS** wide shot — full subject in environment; establishes geography.
- **EWS** extreme wide — scale, crowds, cities; openings, endings, consequences.
Grammar: establish WS → work MS/CU → detail ECU → release WS. Never cut WS→WS or CU→CU of the same subject at the same angle (slideshow tell); change size or angle by ≥30° between adjacent shots of the same subject.

## Angles (name one)
Eye-level (neutral truth), low angle (power, threat, scale), high angle (vulnerability, defeat), over-the-shoulder (following a character's discovery), POV (the audience does it), Dutch tilt (rare; instability only), top-down (systems, maps, mechanisms).

## Movement (exactly ONE per shot, always motivated)
- **Push-in / slow dolly in** — realisation, rising stakes. **Pull-back** — reveal, consequence, loneliness.
- **Tracking / follow** — journey, pursuit of a goal. **Lateral slide** — passing time, scanning a system.
- **Pan** — connecting two things in one space. **Tilt** — scale (feet → tower), or fall (tower → empty street).
- **Crane up/down** — openings (descend into the world) and endings (rise away from it).
- **Handheld micro-movement** — urgency, documentary realism (use sparingly).
- **Locked-off** — deadpan, bureaucracy, a door that does not open; stillness is a choice, say so.
Movement must start and end on a composed frame, at one constant speed, and serve the line being spoken. “Camera slowly zooms and pans and rises” = reject and rewrite.
**Zoom is not in the LedgerFilms movement vocabulary.** A zoom flattens the image and reads as a slideshow effect; achieve emphasis with a dolly/push-in (parallax, real depth) or a cut to a closer size. The single exception: one motivated in-shot zoom at a realisation beat, flagged in the screenplay as deliberate. Editor-side Zoom In filters and Fast Cut zoom transitions are banned outright (see editing.md).

## Light & grade (continuity tools)
One motivated source per scene (window, desk lamp, screen glow), direction kept consistent when returning to a location. LedgerFilms grade: muted teal-and-amber, dramatic motivated light, shallow depth of field, film grain. Time-of-day is a story device: dawn = beginnings, noon = exposure, dusk = turns, night = consequences.

## Prompt formula
`[Character/object block, verbatim from the Bible] + [ONE specific action, present tense] + [shot size] + [angle] + [ONE movement] + [location block] + [light] + cinematic photorealistic AI illustration, dramatic motivated light, muted teal-and-amber grade, shallow depth, film grain, no text, no watermark`

## Data & context discipline (OWNER CORRECTION 2026-11-07 — AI Sell-Off proof rated 6/10: “cinematography needs to be improved, for data better infographics and context required”)
- **Motif ration:** the film's motif shot (here: red line on dark glass) may carry at most ~⅓ of any sequence. A proof where half the shots are the same glass-and-line composition reads as one location, however good each frame is.
- **Ground every abstraction:** within any 3 consecutive clips, at least one shot is human-scale context — a person, a workplace, a town — showing the world the number is about. Data floating over abstract art with no ground under it is a gate failure.
- **Variety is enforced, not hoped for:** across any 10 shots use ≥4 camera behaviours AND ≥3 angles (eye-level alone does not count as variety); crane, low-angle power, high-angle vulnerability, OTS discovery and top-down systems shots exist to be used where the line earns them. If the contact sheet looks like one room, the cinematography failed even if correlation passed.
- **Data lines are shot as graphics, not B-roll:** a line carrying a load-bearing figure is planned as a GRAPHIC beat (see motion-graphics.md) — build, diagram, map or document push — with the location/character context in the same sequence.

## Continuity mechanics
Repeat the full character and location blocks in every prompt (AI generators have no memory). Same seed/reference route whenever the tool offers one; regenerate any shot whose wardrobe, prop or geography drifts. Screen direction: a character travelling left→right keeps travelling left→right across cuts; doors open the same way every time.
