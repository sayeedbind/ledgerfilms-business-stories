# PLAYBOOK — LedgerFilms Business & Money Stories (v1.0)

The full production instructions. `SYSTEM-PROMPT.md` loads this file. When this file and a
user message disagree, the user wins. When this file and an upstream playbook disagree,
this file wins — it is the LedgerFilms adaptation.

**Channel:** LedgerFilmsHQ · AI-Illustrated Business & Money Stories
**Formats:** Long-form ~10:00, 16:9 · Shorts 45–60 s, 9:16 · Nothing else. Never 1:1.
**Look:** cinematic AI art (photoreal-cinematic), faceless, narration-led.

---

## 1. Intake

Ask once, together (see SYSTEM-PROMPT Step 0): **Mode, Topic, Angle, Sources.**
Defaults if unanswered: Mode = what the topic implies (a company saga → long-form; a single
surprising fact → Short), Angle = "the hidden mechanism that made / lost the money",
Sources = research it yourself. Never ask a second round of intake questions — start.

## 2. Research & fact-check (before a single word of script)

1. Build a **research brief** (`templates/research-brief.md`): timeline, 5–12 load-bearing
   facts, the money mechanism, the turning point, the human stakes.
2. **Two-source rule:** every load-bearing fact (money figures, dates, market share,
   quotes, cause of a collapse) needs 2 independent sources; prefer 1 primary —
   SEC filing / annual report / earnings transcript / court or regulator document /
   the company's own archive.
3. Record source + date for each fact in the brief. Figures get their year in the script:
   "by 2019, revenue had fallen to…" — never a naked, timeless number.
4. **Kill or flag:** a fact with one weak source is either cut, softened to what the source
   supports ("reportedly", attributed), or escalated to the user. Never narrate it flat.
5. **Legal pass** for Collapses & Scams topics: name what is *convicted*, *charged/alleged*,
   *regulator-found*, or *reported* — those are four different sentences. No motive claims
   about living people without a source. Full rules: `docs/fact-check-and-legal.md`.
6. No investment advice, no "what I'd do", no price targets — in script, description or
   pinned comment.

## 3. The story spine (both formats)

Every LedgerFilms story answers **one question** and reveals **one mechanism**:

> How did the money actually move — and what did everyone miss until it was too late / obvious?

Beats: **Hook** (a number, a contradiction, or a moment) → **Stakes** (what was on the line)
→ **Origin** (the small beginning) → **Mechanism** (how the money actually worked — the
heart of the video) → **Turning point** (the decision / disruption) → **Climax** (rise peaks
or the fall lands) → **Lesson** (one transferable idea for the viewer's own work/money life —
stated as an observation, never as advice).

Character here means *protagonist*: a founder, a company, or an idea. Give the protagonist
one clear desire and one clear blind spot. That — not dialogue — is what carries a
documentary.

## 4. Scripts

### Long-form (~10 min)
- **1,350–1,500 words** of narration (≈140–150 wpm documentary pace). Write for the ear:
  short sentences, one idea per line in the script file, numbers spelled out as spoken.
- Cold open ≤30 s: the hook + the question, no channel intro, no "in this video".
- A **re-hook every 90–120 s**: a new question, a bigger number, a reversal.
- Chapters follow the spine in §3. End on the lesson + one line that sets up a related
  video (end-screen), never "like and subscribe" in the narration.
- Use `templates/script-long-form.md`.

### Shorts (45–60 s)
- **115–150 words.** One fact, one mechanism, one reveal. Nothing else.
- 0–3 s hook: the contradiction or number, mid-action visual, no setup.
- **Reveal at ~70%** (≈35–42 s) — this replaces the mini-drama "twist": the hidden fee,
  the real customer, the clause, the decision that doomed them.
- Final line either **loops** back to the first line or points to the long-form
  ("the full story is on the channel").
- Use `templates/script-short.md`.

## 5. The Bible (locked before generation)

Build once per video, paste **verbatim** everywhere (`templates/character-and-company-bible.md`):

- **Founder/character block** — age, build, face, hair, one signature item. Use VideoExpress
  **+ Consistent Character** with a dedicated master image, generated and approved first;
  the master is never replaced by a scene image.
- **Era & outfit block** — period-correct clothing, tech, cars, signage. A 1998 scene has
  no smartphones; a 1970s office has no flat screens. Era errors are QC failures.
- **Company block** — logo treatment described as shapes/colour (never ask the model to
  render real logo text), brand colours, product, storefront/office look.
- **Location blocks** — fixed layouts: landmark positions, neighbouring objects, distances,
  camera side. Recurring locations repeat exactly; reject mirrored or swapped sets.
- **Style line** — the channel anchor, in every prompt:
  `cinematic photorealistic AI illustration, dramatic motivated light, muted teal-and-amber
  grade, shallow depth, film grain, no text, no watermark`.
- **Numbers rule:** never ask the image model to render charts, figures or readable text —
  it will garble them. Charts/graphs are abstract shapes in scenes, and real numbers are
  added as clean overlays at edit/upload-prep stage from the research brief.

## 6. Prompt pack (per video)

Use the VideoExpress multishot format — one self-contained prompt per generation,
start-image prompt first, then the video prompt. Full template and worked example:
`skills/ledgerfilms-business-stories/references/multishot-prompt-format.md`
(adapted from the upstream VideoExpress Scripting skill method — see LICENSE-NOTICES.md).

Per generation: `[REFERENCE USE] [IDENTITY / CONTINUITY] [SCENE] [ACTION] [CAMERA]
[LIGHT AND IMAGE] [PRODUCTION SOUND] [NEGATIVES]`, prefixed with its clip ID (`[Clip 07]` /
`[Image 07A]`). Rules that cause the most damage when forgotten:

- The model renders **nouns, not intentions** — every noun you write may appear. Keep
  prompts concrete, countable, and free of stray objects.
- **Positives everywhere except [NEGATIVES]** — the engine reads "no X" outside [NEGATIVES]
  as "include X". Exclusions live only in [NEGATIVES], each starting "No".
- Quotation marks mean **speech**. Our narration is added as narration, so quote nothing in
  visual prompts and keep mouths closed/turned in scenes — no invented dialogue.
- Camera: locked unless the move serves the beat; every move named and given a destination;
  never return to space that has left the frame.
- Plan **continuity handoffs**: for each clip record incoming state → action → outgoing
  state → next clip's opening state. Design the sequence first, generate in order, and
  prepare the next image while earlier clips render.
- Start each clip from a fresh start image at its closest framing by default; chain from a
  previous last frame only when framing matches (chaining compounds drift).

## 7. Generation in VideoExpress

1. **Route:** Long-form/Shorts are narration-led: build scenes as image → video, then the
   narration route for voice: **Narration Video → Create Video → voice → create audio →
   generate video**. Advanced Mode off unless a multi-shot clip needs it; when used, keep
   automatic enhancement OFF and Manual Video Length ON.
2. **Style routing:** channel look = Image Type **Photorealistic (Cinematic)**, Creative
   mode **off**, style line (§5) carried in the prompt text instead.
3. **Re-check settings in the generation dialog itself** before every submission — the
   dialog ratio can reset to 9:16 and enhancement can re-tick after a re-render. The
   project bar being right does not mean the dialog is right.
4. **Concurrency:** submit in scene order, up to the account's visible parallel limit
   (often 5). Full queue = wait for a slot, inspect, submit next. Never duplicate a job.
5. **Retries:** generate each clip once; retry only a confirmed failure or clearly unusable
   output — **max 3 attempts per clip**, changing one variable per retry. Keep usable clips
   despite minor gaze/camera differences; save deep QA for the final pass.
6. Public gallery **off** on everything. No music in any clip.

## 8. Narration & sound

- One narrator: the channel voice, same system voice + settings for every video
  (record them in the bible). Cloned voice only with the speaker's permission.
- **Generate narration once and lock it.** Its real length sets the final runtime —
  the video is cut to the voice, never the reverse.
- Presenter/dialogue audio (rare, only if the user asks for an intro) stays audible;
  all scene-clip audio is **muted under the narration**.
- Music: none in generation; one licensed/library track added at assembly, low, ducked
  under narration, same track family across the channel.

## 9. Assembly & the dead-air trim

1. Media Library → My Media → My AI Videos; add clips to the timeline **in planned scene
   order**, verifying one clip lands before adding the next; no duplicates.
2. Place narration to start at frame 1 (long-form) — no presenter gap by default.
3. **Auto Align Clips**, then the trim pass: at timeline zoom ~40 px/s, cut and delete
   every frozen or silent head and tail; close every gap. In Shorts, no shot may outlive
   its narration line.
4. If footage overruns the narration's right edge: playhead at the audio edge, select the
   last video clip, Cut, delete only the excess right-hand chunk. Never stretch, speed or
   pad the audio to match the picture.
5. Add number/graphic overlays from the research brief (clean text, double-checked against
   sources). Save the project with the naming rule: `LF-YYYYMMDD-topic-slug` /
   `SH-YYYYMMDD-topic-slug`.

## 10. Export & handoff

- Long-form: **High / FullHD 1920×1080 / MP4**. Shorts: **High / FullHD 1080×1920 / MP4**.
- Verify the export exists in My Videos (a submitted export is not a finished export),
  then download/archive it the same day.
- Hand the user, in one message: download link · 3 title options (pick marked) ·
  description (with sources + disclaimer) · tags · pinned comment · end-screen target ·
  thumbnail brief (3 words max on the thumbnail, one cinematic frame, one emotion).
- Run `templates/qc-checklist.md` first. If a check fails, say which and fix it — don't
  ship silently.

## 11. Repurposing (the weekly system)

The week's long-form is researched once and mined three ways:
2 Shorts are **cut-downs** (the mechanism in 60 s; the fall in 60 s), re-framed 9:16 from
the same bible and narration voice — not cropped 16:9 exports. 2 Shorts are **standalone**
hooks on next week's topic and end by teasing it. Full method:
`workflows/repurpose-long-to-shorts.md`.
