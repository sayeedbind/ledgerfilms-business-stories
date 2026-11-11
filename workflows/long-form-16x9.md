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
   **Coverage math first (PLAYBOOK §6):** split the screenplay into **narration beats
   of ≤10 s**, each sized to the dialog's voiceover field (plan ≤~20 words /
   ≤120 characters, one idea per beat) — **one beat = one clip = one voiceover line**.
   Scene count = beat count + ~10% safety B-roll (a 1,400-word script ≈ 70 beats,
   plan ~77). Each pack entry carries TWO texts: the video prompt (visual only) and
   the voiceover text (that beat's exact AUDIO line). A scene plan whose beats
   cannot cover the script is a planning error — fix the count here, not at export.
   Continuity handoff noted per clip (incoming → action → outgoing → next opening).
6. **Generate — voiceover WITH each clip** → image first, then in the generation
   dialog enter the video prompt **and** that clip's voiceover text in the
   voiceover / audio option, locked channel voice selected, and generate. In scene
   order, ≤ account's parallel slots. Settings checked in-dialog every time
   (ratio 16:9, enhance OFF, gallery OFF, **voiceover field filled + voice
   checked**). Max 3 attempts per clip. **There is no separate narrate step.**
   Record each clip's **measured** duration; keep a running total; at each segment
   checkpoint play clips back — voice present, locked voice, full line.
7. **(No separate narration step — it happened inside step 6.)** If a clip's read is
   wrong or a name is mispronounced, regenerate **that clip** with the respelled
   word in its voiceover text. Never generate standalone narration.
8. **Assemble** → timeline in clip order (= narration order; no separate narration
   track), verify each clip, Auto Align, dead-air trim pass (never trim through a
   spoken line). **⛔ Coverage gate (PLAYBOOK §9):** every beat present, every clip
   carrying its checked voiceover, summed duration in range — if any part fails,
   STOP, generate the missing/failed clips and reassemble. No export from an
   under-covered timeline.
9. **Overlays** → numbers/charts as clean text overlays from the brief (never model-rendered).
10. **QC** → `templates/qc-checklist.md`, every box. Fix or disclose failures.
11. **Export** → High / FullHD 1920×1080 MP4, verify in My Videos, download same day.
    Project name: `LF-YYYYMMDD-topic-slug`. **Exports cap at 600 s** — if the summed
    runtime exceeds it, trim to ≤600 s or export in parts and splice (PLAYBOOK §10);
    then play the exported file itself (start/middle/end + closing line), sample
    every clip's head frame and scan the contact sheet before calling it done.
12. **Upload pack** → `templates/upload-metadata.md` + `templates/thumbnail-brief.md`:
    3 titles (pick marked), description with sources + disclaimer, chapters, tags,
    pinned comment, end-screen = the related video the last narration line sets up.
13. **Mine it** → immediately log the 2 cut-down Shorts in `workflows/repurpose-long-to-shorts.md`.
