# Workflow — Long-form documentary (16:9, ~10 min)

Input: Mode=Long-form + Topic. Output: exported 1920×1080 MP4 + full upload pack.
Rules live in `PLAYBOOK.md`; this is the checklist order of operations.

1. **Intake** → fill `templates/intake.md`. One question, the answer to which the whole
   video serves, written at the top.
2. **Research** → `templates/research-brief.md`. Timeline, mechanism, turning point.
   Two-source rule applied; legal ladder checked for any wrongdoing claims. ⛔ No script
   before the brief's source table is complete.
3. **Script** → `templates/script-long-form.md`. 1,350–1,500 words, cold open ≤30 s,
   re-hook every 90–120 s, chapters on the story spine, lesson ending.
4. **Bible** → `templates/character-and-company-bible.md`. Generate + approve the founder
   master image and one master per recurring location. Lock the narrator voice + settings.
5. **Prompt pack** → `templates/prompt-pack.md` + storyboard (`templates/storyboard-long-form.md`).
   **Coverage math first (PLAYBOOK §6):** generations = ⌈ estimated narration seconds ÷ 9 ⌉
   + ~10% safety B-roll, at 8–10 s per clip (~67–74 generations for ~10 min; ~50–55 for
   7½ min). A scene count that cannot cover the narration at 8–10 s per clip is a planning
   error — fix the count here, not at export. Continuity handoff noted per clip
   (incoming → action → outgoing → next opening). Reuse 15–20% of scenes as motifs/B-roll
   to stay inside the week's hours.
6. **Generate** → image first, then video, in scene order, ≤ account's parallel slots.
   Settings checked in-dialog every time (ratio 16:9, enhance OFF, gallery OFF).
   Max 3 attempts per clip. Record each clip's **measured** duration; keep a running total.
7. **Narrate** → one take of the locked script via the VideoExpress narration route.
   Do not re-record for length; the recorded length is the runtime. **Measure it** —
   that total replaces the step-5 estimate as the coverage target.
8. **Assemble** → timeline in order, verify each clip, Auto Align, dead-air trim pass,
   cut overrun at the narration's right edge only. **⛔ Underrun gate (PLAYBOOK §9):**
   if measured video total < measured narration total − 2 s, STOP — generate the missing
   coverage and reassemble. No export from an under-covered timeline.
9. **Overlays** → numbers/charts as clean text overlays from the brief (never model-rendered).
10. **QC** → `templates/qc-checklist.md`, every box. Fix or disclose failures.
11. **Export** → High / FullHD 1920×1080 MP4, verify in My Videos, download same day.
    Project name: `LF-YYYYMMDD-topic-slug`.
12. **Upload pack** → `templates/upload-metadata.md` + `templates/thumbnail-brief.md`:
    3 titles (pick marked), description with sources + disclaimer, chapters, tags,
    pinned comment, end-screen = the related video the last narration line sets up.
13. **Mine it** → immediately log the 2 cut-down Shorts in `workflows/repurpose-long-to-shorts.md`.
