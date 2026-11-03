# LedgerFilms Filmcraft — Screenplay, Cinematography, Motion Graphics, Story

Why this skill exists: on 2026-11-03 the user rejected a finished LedgerFilms video as “a general slideshow” — narration and scenes had zero correlation, screenplay rated 1/10. The root cause was process: an essay script written first, generic thematic prompts matched to it afterwards, clips generated independently. This skill replaces that process. It is loaded for EVERY LedgerFilms video run, alongside the PLAYBOOK, and its gates are blocking.

## Binding (read first)
This skill is one layer of the LedgerFilms Production Stack (`skills/ledgerfilms-production-stack/SKILL.md` in this repo) and is NEVER loaded alone. A run starts only when the full stack is loaded — PLAYBOOK, this Filmcraft skill, the VideoExpress Scripting LedgerFilms adaptation, and the videoexpress_production skill — and the agent has stated the STACK check line from the stack skill. Delegated work (subagents, browser agents) receives the stack via the DELEGATION BLOCK in the stack skill, pasted verbatim into the assignment. Missing layer = stop and report, never improvise.

## The one law
**The screen shows what the voice says, when it says it.** Every narration line is written together with the shot that depicts it. If a line cannot be pictured literally (an object, an action, a place, a visible change), the line is rewritten until it can — or the shot is an intentional, planned graphic (map, figure, document) built for that line. Thematic mood B-roll under essay narration is forbidden.

## How the three skills stack (no overlaps, no gaps)
- **PLAYBOOK = channel law.** Formats, fact discipline, coverage gate, publish rules. It decides WHETHER and WHEN.
- **Filmcraft (this skill) = creative law.** Story spine, two-column screenplay, cinematography, motion graphics. It decides WHAT each shot is and WHY — the screenplay is the single creative source.
- **VideoExpress Scripting (repo adaptation, `skills/videoexpress-scripting/SKILL-ADAPTATION.md` + `references/multishot-prompt-format.md`) = engine mechanics.** It decides HOW a screenplay row becomes a VideoExpress generation: prompt pack with stable IDs, Core Bible blocks verbatim, tagged start images first, timed multi-shot [ACTION] sections, [CAMERA] with a destination, chaining via Save Last Frame, [NEGATIVES] discipline, failure-fix loop. The upstream skill itself is CC BY-NC 4.0 and is NOT installed in this environment — only our original-wording adaptation is used, and commercial reliance on the upstream itself needs the author's permission.
- **`videoexpress_production` skill = session mechanics.** Fragile-session discipline: dedicated profile, short verified segments, save-by-Open-list-timestamp, inventory/count gates.
Translation rule: Filmcraft screenplay row → one pack entry: `[Image NA]` tagged start image → `[Clip N]` multishot prompt whose timed SHOTs are that row's visual, whose [CAMERA] is the row's camera, and whose narration line is the row's AUDIO cell. If a screenplay row cannot be translated, the row is rewritten — the engine never gets a vaguer version of the film. Feature facts and adopted VE behaviours live in `references/videoexpress-capabilities.md` (checked 2026-11-03; re-check the changelog each run and update it).

## Workflow (replaces essay-first scripting)
1. **Story build first** — beat sheet per `references/story-structure.md`: hook, stakes, mechanism, escalation, turn, payoff. One narrative spine, one recurring visual motif, characters with a goal and an obstacle.
2. **Two-column AV screenplay** — per `references/screenplay.md`. Left column: the exact visual (shot size, camera, subject, action, location, continuity notes). Right column: the exact narration line that plays over it. Neither column is written without the other.
3. **Shot list / prompt pack (scripting-skill mechanics)** — start images FIRST: one tagged start image per shot/sequence, candidate passes reviewed, then the clip prompt in the repo's multishot format, with the screenplay's shots as timed [ACTION] segments (hard cuts inside one generation where a sequence belongs together), [CAMERA] one move with a destination, Bible blocks verbatim, style anchor at the start and in [LIGHT AND IMAGE]. Chain sequences with Save Last Frame where the film stays in one space. Camera language per `references/cinematography.md`; engine facts per `references/videoexpress-capabilities.md`.
4. **Motion graphics plan** — per `references/motion-graphics.md`: numbers, dates, quotes and mechanisms that cannot be filmed become planned graphics (figure builds, simple diagrams, document pushes), timed to the line that names them — never decoration.
5. **Proof segment gate** — build the first 60–90 seconds ONLY, export it, and get the user's rating before any full production. No exceptions after the 2026-11-03 rejection.
6. **Full build** — only after the proof passes. Assemble with Fast Cut transitions OFF (VideoExpress has no dissolve; clean cuts), narration locked, coverage gate from PLAYBOOK §9 unchanged.
7. **Editing pass (mandatory before export)** — per `references/editing.md`: topic check, angle audit (multi-angle cinema, no zoom-style motion), sync audit, sound audit, transitions audit, coverage re-check. The owner can invoke it any time with the words “Edit pass”.

## Blocking QC gates (a “no” stops the run)
- **Correlation gate:** pick any 5 random narration lines. For each, can a viewer say what the line was about from the picture alone, muted? If any line fails, the screenplay goes back, not the render queue.
- **Continuity gate:** same character design, wardrobe, locations, props and colour grade across every shot that shares them; a shot that breaks continuity is regenerated, not shipped.
- **Topic gate:** the beat sheet states the topic's central question; every sequence must visibly advance it. A sequence that serves only itself is cut, however good it looks.
- **Camera gate:** every shot names a size, an angle and exactly one motivated movement (or a deliberate locked-off), and the [CAMERA] choice must be justified by that row's narration line — cinematography follows the script and voiceover, never decorates over them. Two adjacent shots never repeat the same size+angle (the classic slideshow tell).
- **Editing gate:** every sequence is covered from ≥3 distinct angles/sizes; any 10 consecutive shots use ≥4 different camera behaviours; zoom-style motion (Zoom In filter, Fast Cut zoom, push-in as a default) is absent except a single motivated in-shot choice. Verified by the EDIT PASS in `references/editing.md` before export.
- **Motif gate:** the visual motif appears in the hook, the turn and the payoff, changed each time (e.g. a door: open → closing → closed/locked open).
- **Mute test:** the proof segment must make sense watched muted. **Audio-only test:** the narration must never describe something the picture contradicts or ignores.

## What “learned” means here
These files are the persistent craft standard: they are re-read at the start of every run, applied in the screenplay and shot list the user can inspect, and checked by the gates above. Improvements from each user review get written back into these references, so a correction is never paid for twice.
