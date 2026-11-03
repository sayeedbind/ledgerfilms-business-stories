# VideoExpress capabilities — adopted into Filmcraft

Checked 2026-11-03. Sources, in reliability order: (1) our own verified hands-on runs in the user's account (VideoExpress 3.5, All Access); (2) the upstream VideoExpress Scripting skill's changelog (v2.6.0, 2026-10-30 — it tracks VE features closely; the skill itself is CC BY-NC 4.0, used here as feature reporting, not copied method text); (3) VideoExpress 3.0 feature coverage. VideoExpress publishes no detailed public changelog of its own that we could find — anything not in (1) is marked “verify in-app on next run”.

## Generation
- **Multi-shot generations (core adoption).** One clip can contain several timed shots with explicit hard cuts, written as timed segments in the prompt (SHOT 1 0–3s wide … SHOT 2 3–6s medium, hard cut …). This is how a screenplay sequence becomes ONE generation with an internal cut rhythm instead of disconnected singles. Never pair it with “one continuous shot” in the same prompt — the instructions fight.
- **Start image is the real anchor.** A clip sees only its opening frame + its prompt — not the reference photos. Continuity therefore runs: master references → tagged start image ([SUBJECT] [FRAMING AND POSITION] [BACKGROUND] [LIGHT AND STYLE] [NEGATIVES]) → clip. Start images get candidate passes and user/agent keep-ditch review before the clip is generated.
- **Consistent Character affects Create Image only** — it never applied to clips (upstream correction, 2026-10-13). Use it to build character/location masters and start images; never rely on it inside a video prompt. Reference Photo 1 = character master, Reference Photo 2 = empty location master where the flow offers both.
- **Chaining.** Save Last Frame of an accepted clip becomes the next clip's start image, so a sequence can play as one continuous space. Plan framing so a clip ends where the next begins; detail redraws when pushing in closer than the size last drawn — closer framing = new start image.
- **Camera from prompt.** Shot size, angle and one movement are prompt language ([CAMERA] block, destination always named). The editor also has timeline filters (Camera Pan, Zoom In, Change Speed, Opacity, Resize and Move, fades, Titles, Green Screen) — LedgerFilms rule: Zoom In filter and Fast Cut Zoom stay OFF permanently; fades are for graphics/audio, not fake camera moves.
- **Clip length.** Manual Video Length ON, beats ≤10s (All Access clips measure ~8–15s depending on route — always measure, PLAYBOOK §6 math unchanged).

## Voiceover / audio
- **Narration routes:** standalone Text to Speech panel (our locked route: Emotion Andrew Multilingual, speed 1, pitch 0, chunks ≤1,000 chars), Narration Video, Voice Recorder, Import Audio, Voice Changer (consistent character voices from a sample — dialogue only; our narration is a single locked TTS voice, so Voice Changer is not needed unless a character ever speaks).
- **Line-per-clip sync option (adopted pattern):** VE's narrated-story format attaches one narration line per clip, then Add to Timeline + Auto Align — sync is structural instead of measured after the fact. For LedgerFilms, group narration by shot-group and verify chunk order by opening words.
- **Production sound:** written per segment in [PRODUCTION SOUND] — transient, action-tied, no music, never “silence”. Clip track ducked under narration in assembly.

## Editor / assembly
- Add to Timeline appends (it lands after existing content — shift/Auto Align to frame 1, as learned 2026-11-02); Auto Align Clips closes gaps; Fast Cut panel exists per track — transitions OFF (styles are only Zoom/Rotation; no dissolve exists in VE 3.5).
- Screen Recorder captures a tab/window into the library — available if a real interface must be shown; not part of the standard faceless workflow.

## QC method adopted
- **Take review by contact sheet:** sample ~12 frames across a take plus its sound profile before accepting it — check opening/ending frames, action beats, camera move, drift, and whether planned sounds land. A take that fails the correlation or continuity gate is re-generated via the failure-fix loop (diagnose the mechanism → fix the rule in the pack globally → sweep sibling clips → one-variable test series if it survives two rewordings), never by blind re-rolls.
