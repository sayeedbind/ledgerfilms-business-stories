# PLAYBOOK — LedgerFilms Business & Money Stories (v1.15)

The full production instructions. `SYSTEM-PROMPT.md` loads this file. When this file and a
user message disagree, the user wins. When this file and an upstream playbook disagree,
this file wins — it is the LedgerFilms adaptation.

**Channel:** LedgerFilmsHQ  
**v1.15 change (2026-11-11, sync of the studio repo's v1.2.0 bundle):** the **CONTEXT STANDARD** is now channel law (§§3–4 + filmcraft `references/context-standard.md` + a blocking **Context gate**): literal referents, mechanism diagrams, system-map opener, tour-guide narration, viewer's-life bookends — written after the owner rated the finished AI Sell-Off long-form 5/10, “still lack of context”, against the FactZaara oil-tanker benchmark. The **SINGLE-VOICE RULE** is named (§8): the video prompt is visuals-only and **Video Only (No Sound) stays OFF**, after a Short shipped with doubled narration. The **600-SECOND EXPORT CAP** + the full verify-the-export law land in §10 (head-frame sample on every clip, contact-sheet uniqueness scan, tail listen). Filmcraft also gains the 2026-11-07 data & context discipline and figure rule, and the proven locked-voice respellings (2026-11-11). Creative mode OFF, the per-clip voiceover route (v1.13) and the DURATION RULE (v1.14) are unchanged and re-affirmed. · **v1.14 change (2026-11-04, owner restated):** the **DURATION RULE** is now named and blocking — **video duration depends on voiceover runtime**: a clip's length is its voiceover's actual runtime, and the video's runtime is the sum of its clips' voiceovers. Never preset a narrated clip's length, never trim/speed a voiceover to fit a preset length, and derive any timed shot segments from the line's words (§§6–7). · **v1.13 change (2026-11-04, owner directive):** **voiceover is made WITH each clip** — every clip is generated from two fields in the VideoExpress generation dialog: the **video prompt** (the visual) and the **voiceover / audio prompt** (that clip's exact narration line, in the dialog's voiceover option, with the one locked channel voice). There is **no separate narration generation, no standalone Text-to-Speech chunks, and no separate narration track** (§§6–9). Clip length follows its voiceover playtime automatically. · **v1.7 change (2026-10-31):** **scene length follows the voiceover** — narration is split into ≤10 s beats and each clip is generated at its beat's measured duration (a 5 s line = a 5 s scene); scene count = beat count + ~10% B-roll (§6). · **v1.6 changes (2026-10-30):** trending topics are presented as a **top-5 rated slate and the user chooses one before production** (§1A) · clip duration supports the **full 10 s** the dialog allows — plan scenes to use it (§6) · **sound follows the upstream reference repos**: clips are generated WITH their described production sound and ducked under the narration, never silent video (§8). · AI-Illustrated Business & Money Stories
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

**Context structure (the Context Standard — full text in filmcraft
`references/context-standard.md`):** the spine is **one thing travelling through one
system** (a dollar, a megawatt, a vote, a chip, a loan). Open with a **system map** — a
single shot or diagram showing every place the story will visit and how they connect —
and return to it at chapter turns. Bookend the film on the **viewer's own daily life**:
the hook starts from something they touch daily (their bill, their app, their rent, the
price at the till) and the lesson returns to exactly that spot.

## 4. Scripts

### Long-form (~10 min)
- **1,350–1,500 words** of narration (≈140–150 wpm documentary pace). Write for the ear:
  short sentences, one idea per line in the script file, numbers spelled out as spoken.
- Cold open ≤30 s: the hook + the question, no channel intro, no "in this video".
- A **re-hook every 90–120 s**: a new question, a bigger number, a reversal.
- Chapters follow the spine in §3. End on the lesson + one line that sets up a related
  video (end-screen), never "like and subscribe" in the narration.
- Use `templates/script-long-form.md`.
- **Context rules (the Context Standard — a finished film was rated 5/10 for breaking
  these; they bind Shorts too):** every noun the narration names appears on screen **as
  itself** in the same beat — a symbol or mood shot may accompany a fact, never carry it.
  **One fact per line**; a line packing three facts becomes three lines and three shots.
  Write as a **tour guide**, not an essayist: "this…", "here…", signposted chapter turns,
  questions the next shot answers. Every **invisible mechanism** (inside a market, a
  machine, a law, the ground) gets a planned **diagram beat** — cross-section, cutaway or
  flow diagram with the process moving inside it; a figure overlay is not a mechanism.
  Every abstract mechanism gets an **everyday analogy**. Show the **humans** — faces,
  routines, danger — don't just state them. The screenplay must pass the filmcraft
  **Context gate** (muted, any 5 lines: WHAT / WHERE in the system / HOW does it work)
  before generation.

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
- Quotation marks mean **speech**. Quote nothing in **visual** prompts and keep mouths
  closed/turned in scenes — no invented dialogue. The narration itself is never
  quoted into the video prompt: it goes, unquoted and verbatim, into the clip's
  **voiceover field** (§§7–8).
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

> **DURATION RULE (owner, restated 2026-11-04): video duration depends on voiceover runtime.** Per clip and for the whole video: the voiceover's runtime comes
> first and the picture follows it. A planned duration is only a word-based
> estimate (words ÷ ~150 wpm) until the clip is generated; the generated
> voiceover's **actual** runtime is the clip's length, final. Never choose a clip
> length first and squeeze the line into it, never set a manual length on a
> narrated clip, and never trim, speed or pad a clip's voiceover to hit a planned
> number — if picture and voice disagree, the voice wins and the picture is
> re-timed or the clip regenerated.

1. **Estimate, then measure.** Before generation, estimate narration seconds from the
   script (words ÷ ~150 wpm × 60 for planning). That estimate is for planning only:
   under the per-clip voiceover route (§§7–8) there is no separate narration file to
   measure — each finished clip's **measured duration is its voiceover's duration**,
   and the sum of clip durations is the runtime.
2. **One beat = one clip = one voiceover line.** Split the screenplay into **beats of
   ≤10 s of spoken narration** (one idea per beat, cut at sentence boundaries), and
   size every beat to **fit the generation dialog's voiceover field**: plan
   **≤~20 words / ≤120 characters per clip** until the first generation of the run
   confirms the field's current limit in the dialog, then never exceed the smaller
   of (that limit, ~25 words / 10 s). A line that does not fit is split into two
   beats with two shots — never pasted into a separate TTS tool, never truncated.
3. **Scene count formula:** scenes = **number of narration beats**, plus a ~10%
   safety margin of extra B-roll / motif generations — and every B-roll clip that
   plays under a spoken line carries that line's voiceover too; a truly silent
   B-roll clip is planned as such and counted as picture only. Quick check: a
   1,400-word long-form at ~20 words per beat is ~70 beats, plan ~77 generations.
   A 30-scene plan can only ever cover ~4:00–5:00 — never promise it covers a
   long-form.
4. **Running total while generating:** record every finished clip's **measured**
   duration in the storyboard and keep a running total — that total is picture and
   narration together, by construction. Stop generating only when every beat has
   its clip and the total lands in the format's runtime range. If it falls short,
   the missing beats are generated — never stretch, slow, freeze, loop or pad a
   clip to fake coverage.

## 7. Generation in VideoExpress

1. **Route — voiceover WITH each clip (owner directive, 2026-11-04):** every clip is
   generated in the dialog from **two fields**: (a) the **video prompt** — the visual
   prompt only; and (b) the **voiceover / audio option** — that clip's exact AUDIO
   (narration) line, entered as the clip's voiceover text, with the locked channel
   voice + settings selected in the dialog **before** generating. Generate the audio
   with the video for that clip, every clip, no exceptions. **Never generate the
   narration separately** — no standalone Import Media → Text to Speech chunks, no
   My AI Audio assets, no separate narration track at assembly. Because the voice is
   generated with the picture, **clip length follows the voiceover playtime
   automatically** (the DURATION RULE, §6): **do not set Manual Video Length on a
   narrated clip at all** — its length is whatever its voiceover runs; **measure
   the finished clip** (picture + voice together) and record that as its duration. The old standalone route's failure
   modes — chunk ordering, a narration track displaced past the picture (Anthropic
   export, 2026-11-03) — are designed out by this route. Historical note: Advanced
   Mode ON is still required **only** if a silent / B-roll clip's length must be
   controlled manually (the length control appears only with Advanced Mode ticked,
   owner-confirmed 2026-11-03); keep automatic enhancement OFF.
2. **Style routing:** channel look = Image Type **Photorealistic (Cinematic)**, Creative
   mode **off**, style line (§5) carried in the prompt text instead.
3. **Re-check settings in the generation dialog itself** before every submission — the
   dialog ratio can reset to 9:16, enhancement can re-tick, and the **voiceover field
   / voice selection can reset** after a re-render. Confirm this clip's voiceover
   text is in the field and the locked voice is selected before every Generate
   click. The project bar being right does not mean the dialog is right.
4. **Concurrency:** submit in scene order, up to the account's visible parallel limit
   (often 5). Full queue = wait for a slot, inspect, submit next. Never duplicate a job.
5. **Retries:** generate each clip once; retry only a confirmed failure or clearly unusable
   output — **max 3 attempts per clip**, changing one variable per retry. Keep usable clips
   despite minor gaze/camera differences; save deep QA for the final pass.
6. Public gallery **off** on everything. No music in any clip.
7. **Duration discipline:** each clip's duration is set by **its own voiceover**
   (see §6), and you record each finished clip's **measured** duration in the
   storyboard against its beat. Assumed durations are not evidence — a clip counts
   only for the seconds it actually runs, and a clip whose voiceover is missing,
   truncated, in the wrong voice, or does not match its AUDIO line does not count
   at all: regenerate that clip.

## 8. Narration & sound — voiceover made with each clip

- One narrator: the channel voice, same system voice + settings for every clip of
  every video (currently **Emotion Andrew Multilingual, speed 1, pitch 0** — record
  them in the bible; any change is an owner decision). Cloned voice only with the
  speaker's permission.
- **Route (owner directive, 2026-11-04): the generation dialog's voiceover / audio
  option, per clip.** In VideoExpress each generation shows a **video prompt** and
  an **audio / voiceover prompt** for that clip. Put the visual in the video prompt;
  put that clip's **exact AUDIO line** in the voiceover field; select the locked
  voice + settings; generate — the clip comes back with its voiceover already on
  it, at the voiceover's length, in sync by construction. Repeat for every clip.
- **Never separate again.** No standalone Text-to-Speech generation, no
  ≤1,000-character chunks, no My AI Audio narration assets, no dragging narration
  onto a timeline track, no re-aligning voice to picture at assembly. The retired
  route (2026-10-30 → 2026-11-04) is history, not a fallback: if the voiceover
  option is missing or fails on a clip, stop and report it — do not fall back to
  separate narration without the owner's say-so.
- **Fit the field.** Size each beat to the voiceover field's limit (§6): plan
  ≤~20 words / ≤120 characters per clip, verify the current limit on the run's
  first clip, and split any longer line across two beats/shots. Never truncate a
  line to fit, and never put the narration text inside the video prompt.
- **THE SINGLE-VOICE RULE (corrected by the owner, 2026-11-07 — a Short's first
  version shipped with every line said twice):** the video prompt describes
  **visuals only** — never the narration line, never quoted speech, never
  "narrator says" — because the video model voices any line it is given, and the
  clip's voiceover then says it a second time (doubled narration). The
  visuals-only prompt is the kill switch. **"Video Only (No Sound)" stays OFF**
  on narrated clips: ticking it kills ALL audio, including the voiceover (proven
  on the repair run — a clip generated with it ticked came back silent).
- **Locked means per-clip locked.** Once a clip is accepted, its voiceover is not
  re-recorded, cut, sped up or swapped. A mispronunciation or wrong read is fixed
  by **regenerating that one clip** with the respelled word in its voiceover text
  (screenplay pronunciation list) — never by patching a separate audio track.
- **Verify voice on every clip** at the segment checkpoint: play the clip — voice
  present, correct voice, full line, no truncation, picture matches the line —
  and **listen to the clip's tail** for a doubled final word or a second voice
  starting under the first (the doubled-narration defect passes a
  words-present-and-in-order check; only the tail listen catches it). A
  silent or mismatched clip is a failed clip (max 3 attempts, one variable changed
  per retry), not an assembly problem to fix later.
- **Clip sound:** every clip is still **generated with the production sound
  described in its [PRODUCTION SOUND] block** — transient, action-tied ambience
  and effects, no dialogue, no music — mixed low under that clip's voiceover,
  never competing with it.
- Music: none in generation; one licensed/library track added at assembly, low, ducked
  under the clips' voiceovers, same track family across the channel.

## 9. Assembly & the dead-air trim

1. Media Library → My Media → My AI Videos; add clips to the timeline **in planned scene
   order**, verifying one clip lands before adding the next; no duplicates. There is
   **no separate narration track to build** — every clip already carries its own
   voiceover (§8). If a drop lands nowhere, the target track is probably clipped
   below the viewport: raise the browser viewport height or close the media panel.
   Never clear a track with its header bin — it deletes the whole track row
   (reload restores the default two-track layout).
2. The first clip starts at frame 1 (long-form) — its voiceover is the opening line,
   no presenter gap by default. Clip order **is** narration order: verify the
   sequence against the screenplay before aligning.
3. **Auto Align Clips**, then the trim pass: at timeline zoom ~40 px/s, cut and delete
   every frozen or silent head and tail **that carries no voiceover**; close every
   gap. Never trim through a spoken line. In Shorts, no shot may outlive its line.
4. If the assembled total overruns the format's range, cut whole beats (picture +
   their voiceover together) or re-plan — never stretch, speed, or pad audio, and
   never cut a clip's voiceover off mid-line.
5. **⛔ BLOCKING coverage gate — check before saving as final and before any export:**
   (a) **Count:** every planned beat has its clip, in order, no duplicates;
   (b) **Voice-per-clip:** every clip's voiceover is present, in the locked voice,
   complete, and matching its AUDIO line (check at segment checkpoints and again
   on the assembled timeline — a silent, truncated or wrong-line clip fails the
   gate); (c) **Runtime:** the summed measured clip durations land in the format's
   range (long-form ~9–11 min; Short 45–60 s). If any part fails, **STOP. Do not
   save as final, do not export, and do not report the video as finished.** Go back
   to §6/§7, generate the missing or failed clips (with their voiceovers),
   reassemble, and re-check. A frozen frame, a black tail, a looped clip or a
   slowed clip is not coverage. (This gate replaces the old video-vs-narration
   totals check: under the per-clip route the two totals are the same number —
   what can still fail is a missing beat or a clip without its voice.)
6. Add number/graphic overlays from the research brief (clean text, double-checked against
   sources). Save the project with the naming rule: `LF-YYYYMMDD-topic-slug` /
   `SH-YYYYMMDD-topic-slug`.

## 10. Export & handoff

- **⛔ THE 600-SECOND EXPORT CAP (learned 2026-11-08, cost the AI Sell-Off film its
  closing line):** VideoExpress exports are hard-capped at **600 s** — the dialog
  warns "The duration of your project exceeds the allowed duration (10 minutes).
  Your movie will be reduced." and the render cuts at exactly 600.00 s, **silently
  dropping the end**. Any project over 600 s must be trimmed to ≤600 s before
  export, or exported in parts and spliced locally (the AI Sell-Off fix: clip 119
  spliced back at the measured boundary in the local finishing pass). Whichever
  route: verify the closing line is present in the exported file itself.
- Long-form: **High / FullHD 1920×1080 / MP4**. Shorts: **High / FullHD 1080×1920 / MP4**.
- Verify the export exists in My Videos (a submitted export is not a finished export),
  then **play the export itself** at the start, middle and end: picture present,
  voiceover present **on the picture** and matching the scene at each point.
  Existence and file size are not verification. The full verify-the-export law:
  sample a frame from the **head of every clip** (a clip once opened on ~2.5 s of
  black in the raw export and every segment check missed it — head frames are
  sampled, never assumed), scan a **contact sheet for repeated visuals** across
  clips (the CVS Short was rejected for the same clips/images in at least 3 clips
  after a sync-only check passed it), and **listen to each clip's tail** for
  doubled audio (§8). Then
  download/archive it the same day. The handoff must state the measured total
  runtime, the clip count, and confirm the §9 coverage gate passed (every clip
  carrying its voiceover); an export with voiceover missing, displaced past the
  picture, or running over black is a failed export, not a finished video.
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
the same bible and the same per-clip voiceover route and locked voice — not cropped 16:9 exports. 2 Shorts are **standalone**
hooks on next week's topic and end by teasing it. Full method:
`workflows/repurpose-long-to-shorts.md`.
