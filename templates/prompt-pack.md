# Prompt pack — [video title] ([LF/SH]-YYYYMMDD-slug)

## Overview
- Format: 16:9 long-form / 9:16 Short · Target runtime: · Generation count: ·
- **Coverage math (PLAYBOOK §6, mandatory):** estimated narration ___ s ·
  one beat = one clip = one voiceover line (line sized to the dialog's voiceover
  field, plan ≤~20 words / ≤120 characters; clip length follows its voiceover) ·
  narration beats = ___ · B-roll margin +10% = ___ · planned clips: ___ ·
  planned generations ___ · measured running total (sum of finished clips) ___ s
- Bible: `templates/character-and-company-bible.md` instance → (link/copy location)

## Global rules for this pack
- Style line, negatives and bible blocks: verbatim (see bible file).
- Settings every submission: ratio ___ checked in-dialog · enhance OFF · gallery OFF ·
  Creative mode OFF · Image Type Photorealistic (Cinematic) · **voiceover field filled
  with this clip's line + locked voice (Emotion Andrew Multilingual, speed 1, pitch 0)
  selected**.
- Fresh start image per clip unless the storyboard marks CHAIN (same framing only).

## Per clip
### [Image 01A] — start image
Settings/refs: Ref 1 = founder master · Ref 2 = location master · Consistent Character ON
```
<start-image prompt, starting with the clip's style line, bible blocks verbatim>
```
### [Clip 01] · 0:00–0:09 · FRESH from Image 01A · role: cold open
**Two fields in the generation dialog — paste each into its own field:**
- **Video prompt** → the block below.
- **Voiceover / audio prompt** → `[VOICEOVER]` line below (locked voice selected in the dialog).
```
[Clip 01]
[REFERENCE USE] …
[IDENTITY / CONTINUITY] <bible blocks verbatim>
[SCENE] …
[ACTION] Total duration ≈9s (= this clip's voiceover runtime, estimated from its line — DURATION RULE: the generated voiceover's actual runtime is final). SHOT 1 (0–3s, …): … SHOT 2 (3–6s, hard cut, …): … SHOT 3 (6–9s, hard cut, …): …
[CAMERA] …
[LIGHT AND IMAGE] <style line> …
[PRODUCTION SOUND] … (transient, action-tied only; no music)
[NEGATIVES] No …
```
`[VOICEOVER]` <this clip's exact AUDIO line — paste into the dialog's voiceover field, NOT into the video prompt above>
Continuity: incoming ___ → outgoing ___ → next clip opens ___.
Voiceover checked on finished clip (present · locked voice · complete line): ☐

<!-- Repeat per clip. Keep IDs stable; cut clips leave gaps (note them), alternates get a
letter suffix ([Clip 07B]) with their own start image. -->

## Edit / timing / QC notes
- Overlays to add (numbers, dates) with brief fact #:
- Open items:
