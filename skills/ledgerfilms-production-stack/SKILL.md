# LedgerFilms Production Stack — the binding

This skill binds the LedgerFilms skills into ONE mandatory load for every agent on every LedgerFilms video run — Muse (main, side chats, subagents), browser agents, and any external agent (ChatGPT / Claude / Grok) started from the repo's SYSTEM-PROMPT. No agent may run a LedgerFilms video from a subset of the stack. If any layer is missing or cannot be loaded, the agent STOPS and reports which layer is missing — it never improvises a replacement from memory.

## The stack, in load order
1. **PLAYBOOK** (repo `PLAYBOOK.md`) — channel law: formats, fact discipline, coverage gate, publish rules.
2. **LedgerFilms Filmcraft** (`skills/ledgerfilms-filmcraft/SKILL.md` in this repo + its references: screenplay, cinematography, story-structure, motion-graphics, videoexpress-capabilities, editing, finishing) — creative law: two-column AV screenplay, camera language, graphics, the one law (the screen shows what the voice says), blocking QC gates, proof-segment-first.
3. **VideoExpress Scripting — LedgerFilms adaptation** (repo `skills/videoexpress-scripting/SKILL-ADAPTATION.md` + `skills/ledgerfilms-business-stories/references/multishot-prompt-format.md`) — engine mechanics: prompt pack, Core Bible verbatim, tagged start images, timed multi-shot [ACTION], [CAMERA] with destination, chaining, negatives, failure-fix loop. The upstream skill (ratava, CC BY-NC 4.0) is linked, never copied; on platforms where the user has installed it, it may be loaded in this layer's place — flag the licence before commercial reliance.
4. **Production mechanics** (PLAYBOOK §§7–9 and `workflows/` in this repo; in the owner's Muse environment, the `videoexpress_production` custom skill) — session mechanics: dedicated profile, segmented verified saves, inventory/count gates.
Plus, when the topic is Trending/blank: **video_trend_research** (repo trend skill) at §1A.

## Stack check (mandatory, before any scripting or generation)
The agent states one line, in its first working message of the run:
`STACK: Playbook v<version> · Filmcraft loaded <date> · Scripting adaptation loaded (upstream changelog checked: v<version, date>) · Production skill loaded`
A run that cannot produce this line truthfully has not started. The capabilities reference is refreshed from the upstream changelog at this point if it is older than the latest upstream release.

## How the binding travels to other agents
- **Repo agents (any platform):** the repo's SYSTEM-PROMPT Step 1A is the cross-platform binder — it routes agents to the full stack in this repo: Playbook, this stack skill, filmcraft (`skills/ledgerfilms-filmcraft/`), the scripting adaptation and the trend-research skill. An agent that started anywhere else must be handed this stack explicitly.
- **Subagents / browser agents (this environment):** they cannot see the main conversation, so the delegating agent pastes the DELEGATION BLOCK (below) at the top of every assignment, verbatim, and attaches/loads the layer files the worker needs. A worker that reports it could not read a layer is stopped and re-briefed — its output is not used.
- **The owner's Muse chats:** filmcraft and this stack also live as custom skills in the owner's Muse workspace; skill search surfaces them for any LedgerFilms/video task, and the owner's MEMORY.md records the stack as standing context for every future conversation.

## DELEGATION BLOCK (paste verbatim into every delegated LedgerFilms assignment)
```
STACK BINDING — mandatory, no subset: (1) PLAYBOOK = channel law (formats, facts, §9 coverage gate). (2) FILMCRAFT = creative law: the screen shows what the voice says, when it says it; two-column AV screenplay; one shot size + angle + ONE motivated camera move per shot; blocking gates (correlation, continuity, camera variety, motif, mute test); proof segment before any full build. (3) VIDEOPRESS SCRIPTING (LedgerFilms adaptation) = engine mechanics: prompt pack with stable IDs, Core Bible verbatim in every prompt, tagged start image first (a clip sees only its start image + prompt), timed multi-shot [ACTION] with hard cuts, [CAMERA] with a destination, Save Last Frame chaining, [NEGATIVES] only for exclusions, failure-fix by mechanism. (4) PRODUCTION = session mechanics: dedicated VideoExpress profile, segmented saves verified by Open-list timestamp, Fast Cut transitions OFF, voiceover made WITH each clip from the dialog's voiceover option (that clip's line, locked voice — never separate narration, never a separate narration track; DURATION RULE: a clip's length is its voiceover's runtime — never preset it, never trim/speed the voice). (5) SPEED = fast execution, no wasted time: never wait idle (prepare the next step while renders run), batch generations to the visible queue limit, verify only at segment checkpoints, start the next step the moment a step lands, change tactic after the same failure twice. If you cannot load or read any layer, STOP and report which one — do not improvise.
```

## After export (finishing & the retention loop)
Export is not the end of a run. The filmcraft finishing reference (`references/finishing.md`) governs what follows: score/mix and grade finishing, corrected captions and chapters, the upload pack with the YouTube AI-content disclosure ticked (blocking), and the post-publish retention review (~72 h and ~7 d) whose dated lesson is written back into the stack. A run is reported complete only when the finishing checklist in `templates/upload-metadata.md` is filled.

## Speed discipline (owner's rule: fast execution, no wasted time)
1. **No idle waiting.** While a generation or export renders, do the next preparation — next prompts, graphics list, upload pack. Watching a progress bar is a failed step.
2. **Batch to the queue limit.** Fill the account's visible parallel generation slots (often 5); never run strictly one-by-one while slots sit free.
3. **Verify only at checkpoints.** Segment boundaries are where saves, counts and totals are verified — no mid-segment verification navigation (it wastes time and kills VideoExpress sessions).
4. **Chase every finish.** The moment a generation, save or export lands, the next step starts in the same session. A completed sub-step is never a stopping point, and a finished on-site task is verified and reported immediately — the owner monitors live and must never see a finished task sitting idle.
5. **Stall rule.** The same failure twice = change tactic (segment the build, re-sign-in in the same profile, one-variable prompt change). Never loop silently; a clip that fails 3 times is reported (Playbook stop rule).
6. **Report at segment boundaries** with measured totals, so the owner never has to ask what is happening.
7. **Fail small, fail fast.** The proof-segment gate is also a speed rule: a wrong approach must die in 90 seconds of footage, not after a 3-hour full build.

## Precedence
User's explicit instruction > PLAYBOOK (channel law) > Filmcraft (creative law) > Scripting adaptation (engine mechanics) > Production skill (session mechanics). Conflicts are reported, never silently resolved by the lower layer.
