# PLAYBOOK — LedgerFilms Business & Money Stories (v1.3)

The full production instructions. `SYSTEM-PROMPT.md` loads this file. When this file and a
user message disagree, the user wins. When this file and an upstream playbook disagree,
this file wins — it is the LedgerFilms adaptation.

**Channel:** LedgerFilmsHQ  
**v1.6 changes (2026-10-30):** trending topics are presented as a **top-5 rated slate and the user chooses one before production** (§1A) · clip duration supports the **full 10 s** the dialog allows — plan scenes to use it (§6) · **sound follows the upstream reference repos**: clips are generated WITH their described production sound and ducked under the narration, never silent video (§8). · AI-Illustrated Business & Money Stories
**Formats:** Long-form ~10:00, 16:9 · Shorts 45–60 s, 9:16 · Nothing else. Never 1:1.
**Look:** cinematic AI art (photoreal-cinematic), faceless, narration-led.

---

## 1. Intake

Ask once, together (see SYSTEM-PROMPT Step 0): **Mode, Topic, Angle, Sources.**
Defaults if unanswered: Mode = what the topic implies (a company saga → long-form; a single
surprising fact → Short), Angle = "the hidden mechanism that made / lost the money",
Sources = research it yourself. Never ask a second round of intake questions — start.
**Topic may be `Trending`** — that is a real instruction, not a missing answer: it hands
topic selection to §1A.

## 1A. Trend research — pick the topic from live signals (before §2)

Run `skills/ledgerfilms-trend-research/` whenever Topic is `Trending` or blank, when
the user asks what's hot / what to make next, and once before a Full-week slate is
locked. The channel does not take topics from the model's memory when live signals
can be checked.

1. **Scan** Google Trends, YouTube (search + autocomplete), Reddit and at least one
   news/calendar source, in the browser, and record every signal with its link, date,
   timeframe and geography (US first, then UK/CA/AU).
2. **Filter** to the channel pillars with a revealable money mechanism; apply the
   skill's drop list (off-niche hype, rumours, advice bait, legally unbacked claims).
3. **Score** survivors on the skill's 10-factor /50 rubric, fill
   `templates/trend-brief.md`, and present the **top 5 as a ranked slate with each
   item's rating (/50)** — then **STOP and wait for the user to choose one**.
   Production on a trending topic starts only after the user's pick. State each
   candidate's publish-by window — a trend whose window can't fit the cadence is a
   Short or a pass, never a rushed long-form.
4. **User gave a topic instead:** run the skill's light pass only — timeliness and
   the exact phrases viewers are searching — and keep the user's topic. Surface a
   cold/saturated warning once, with evidence, and let the user decide.
5. A trend signal is evidence of **interest, never of facts**. The winning topic goes
   through §2 research and the two-source rule exactly like any other topic. If no
   candidate clears the filter, say so and fall back to the topic bank's best
   evergreen — never promote a weak trend to fill the slot.
6. Save the brief's search phrases: they seed the keyword & hashtag pack that §10
   must deliver at handoff (skill reference `keywords-and-hashtags.md`).

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

### Coverage math — MANDATORY, before any generation (added v1.3)

The blocking failure this prevents: picture that runs out before the narration does
(2026-10-29: 30 short clips totalling ~2:42 against 7:24 of narration — an export that
should never have been made). **Planned scene counts mean nothing; only measured
seconds count.**

1. **Estimate, then measure.** Before generation, estimate narration seconds from the
   script (words ÷ ~150 wpm × 60 for planning). After narration is generated (§8),
   replace the estimate with its **measured** duration — that number is the coverage
   target, and it is final.
2. **Clip length is 8–10 s — up to the 10 s maximum the dialog supports.** Set
   Manual Video Length to the beat's length (max **10 s**) and state the duration in
   the clip's [ACTION]. Scene planning should use the full 10 s where the beat
   allows — more story per generation, fewer clips to juggle. A route that silently
   returns ~5 s clips (e.g. plain Text To Video with no length set) does **not**
   satisfy a plan written for 8–10 s clips — re-plan the count at the measured length.
3. **Scene count formula:** generations needed = ⌈ narration seconds ÷ 9 ⌉ at the
   conservative 9 s planning average (⌈ ÷ 10 ⌉ if every clip is set to the full
   10 s), plus a ~10% safety margin of extra B-roll / motif generations. Worked
   examples: 7:24 of narration (444 s) → at least 50 generations at 9 s, plan ~55
   (⌈444 ÷ 10⌉ = 45 if all clips run 10 s); ~10:00 (600 s) → at least 67 at 9 s,
   plan ~74 (60 at 10 s). A 30-scene plan can only ever cover ~4:00–5:00 at these
   clip lengths — never promise it covers a long-form.
4. **Running total while generating:** record every finished clip's **measured**
   duration in the storyboard and keep a running footage total. Stop generating only
   when the measured total ≥ the narration target. If it falls short, generate
   additional on-topic B-roll / alternate-angle clips for the beats that are short —
   never stretch, slow, freeze, loop or pad a clip to fake coverage.

## 7. Generation in VideoExpress

1. **Route:** Long-form/Shorts are narration-led: build scenes as image → video, and the
   voice via the **standalone Text-to-Speech route — Import Media → Text to Speech**
   (field-tested 2026-10-30: the generation dialog's "Narration Video" flow caps its text
   box at 120 characters and each import replaces the pending audio — it cannot build a
   10-minute voice-over; details in §8). Advanced Mode off unless a multi-shot clip needs
   it; when used, keep automatic enhancement OFF and Manual Video Length ON.
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
7. **Duration discipline:** generate every clip at 8–10 s (see §6 coverage math), and
   record each finished clip's **measured** duration in the storyboard with a running
   footage total. Assumed durations are not evidence — a clip counts only for the
   seconds it actually runs.

## 8. Narration & sound

- One narrator: the channel voice, same system voice + settings for every video
  (record them in the bible). Cloned voice only with the speaker's permission.
- **Route (field-tested 2026-10-30): Import Media → Text to Speech** (the standalone
  panel). Do **not** use the generation dialog's "Narration Video" checkbox: it requires
  a generated start image, caps its text box at **120 characters**, and each Import
  Speech **replaces** the pending audio (closing the dialog loses it entirely).
- **Chunking:** the standalone tool's counter reads 2,400 characters, but imports above
  ~1,100 characters can **fail silently** (2,326 chars → no audio, no error; 699 and
  1,074 chars succeeded). Split the narration into **≤1,000-character chunks** at
  sentence boundaries. Rendering takes ~10 s per ~120 characters.
- **Library assets:** every successful import lands in **Media Library → My Media →
  My AI Audio**, labelled with the chunk's opening words, each with a
  `/library/download/<id>` link. Record asset IDs per chunk in script order — the TTS
  panel row shows only the latest import. The list mixes all past projects: match
  chunks by their opening-words labels, never by grid position.
- **Generate narration once and lock it.** Its real length sets the final runtime —
  the video is cut to the voice, never the reverse. **Measure its duration in seconds
  as soon as it exists and write it into the storyboard/prompt pack** — it is the
  coverage target for the §9 underrun gate. Chunks: sum the measured chunk durations;
  the total is the target.
- **Clip sound follows the upstream reference method** (realistic-mini-dramas,
   videoexpress-two-character-agent): every clip is **generated with the production
   sound described in its prompt** — transient, action-tied ambience and effects, no
   dialogue, no music — never silent video. At assembly that production sound stays
   in the mix, **ducked low under the narration** (not hard-muted), so scenes stay
   alive without competing with the voice.
- Music: none in generation; one licensed/library track added at assembly, low, ducked
  under narration, same track family across the channel.

## 9. Assembly & the dead-air trim

1. Media Library → My Media → My AI Videos; add clips to the timeline **in planned scene
   order**, verifying one clip lands before adding the next; no duplicates. Audio assets
   (narration chunks) are added the same way — **drag-and-drop only**, from My AI Audio;
   a single click only selects. If a drop lands nowhere, the target track is probably
   clipped below the viewport: raise the browser viewport height or close the media
   panel. Never clear a track with its header bin — it deletes the whole track row
   (reload restores the default two-track layout).
2. Place narration to start at frame 1 (long-form) — no presenter gap by default. Drag
   the narration chunks onto the audio track **in script order** (verify each label:
   the asset's name is its opening words).
3. **Auto Align Clips**, then the trim pass: at timeline zoom ~40 px/s, cut and delete
   every frozen or silent head and tail; close every gap. In Shorts, no shot may outlive
   its narration line.
4. If footage overruns the narration's right edge: playhead at the audio edge, select the
   last video clip, Cut, delete only the excess right-hand chunk. Never stretch, speed or
   pad the audio to match the picture.
5. **⛔ BLOCKING underrun gate — check before saving as final and before any export:**
   sum the measured durations on the video track and compare with the measured
   narration duration. If video total < narration total − 2 s, **STOP. Do not save as
   final, do not export, and do not report the video as finished.** Go back to §6/§7,
   generate the missing coverage as additional clips for the short beats, reassemble,
   and re-check. A frozen frame, a black tail, a looped clip or a slowed clip is not
   coverage. (This gate exists because an under-covered export was shipped on
   2026-10-29 — see §6 coverage math.)
6. Add number/graphic overlays from the research brief (clean text, double-checked against
   sources). Save the project with the naming rule: `LF-YYYYMMDD-topic-slug` /
   `SH-YYYYMMDD-topic-slug`.

## 10. Export & handoff

- Long-form: **High / FullHD 1920×1080 / MP4**. Shorts: **High / FullHD 1080×1920 / MP4**.
- Verify the export exists in My Videos (a submitted export is not a finished export),
  then download/archive it the same day. The handoff must state **both** measured
  totals — total footage seconds and total narration seconds — and confirm the §9
  underrun gate passed; an export whose duration was set by narration running past
  the end of the picture is a failed export, not a finished video.
- Hand the user, in one message: download link · 3 title options (pick marked) ·
  description (with sources + disclaimer) · tags · pinned comment · end-screen target ·
  thumbnail brief (3 words max on the thumbnail, one cinematic frame, one emotion) ·
  **the keyword & hashtag pack for every platform** (YouTube long-form, YouTube
  Shorts, TikTok, Instagram Reels, Facebook, X) built by the trend-research skill
  from the scan's real search phrases and filled into `templates/upload-metadata.md`.
- Run `templates/qc-checklist.md` first. If a check fails, say which and fix it — don't
  ship silently.

## 11. Repurposing (the weekly system)

The week's long-form is researched once and mined three ways:
2 Shorts are **cut-downs** (the mechanism in 60 s; the fall in 60 s), re-framed 9:16 from
the same bible and narration voice — not cropped 16:9 exports. 2 Shorts are **standalone**
hooks on next week's topic and end by teasing it. Full method:
`workflows/repurpose-long-to-shorts.md`.
