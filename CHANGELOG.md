# Changelog

## v1.16 — 2026-11-13
- **New skill: LedgerFilms Thumbnails (`skills/ledgerfilms-thumbnails/`) — the
  thumbnail generator the system was missing (owner directive, 2026-11-13).**
  Until now the repo carried thumbnail *rules* only (brief template,
  titles/thumbnails doc, the finishing packaging triangle); finished thumbnails
  were improvised locally per film. The owner designated **Artistly**
  (app.artistly.ai, same provider as VideoExpress; “Artistly Unlimited
  (Full Pay)” account, login in the Secure Vault) as the production tool.
- **Route, verified live before write-down:** the **Advanced AI Image Designer**
  (canvas editor) is the production route — the only place an exact canvas size
  exists (custom Width × Height: **1280×720** long-form, **1080×1920** Shorts
  covers). The headline **Thumbnail Agent is rejected as the route** (YouTube
  URL + quantity only — no prompt, style, size or text control; useless for an
  unpublished video), and the Fast designer's ratios are near-misses (16:9 =
  1344×768). Workflow: brief first (≤3 words, figure checked like any claim,
  title/thumbnail never repeat) → base frame from the **raw** export (before
  burned captions) → exact-size project → frame full-canvas → editor treatments
  (upscaler, object remover, background *replace* — no true remover) → channel
  text (bold, figure in amber **#FFB000** hex, impact word white; heavy face) →
  save + PNG export → **download same day** (Personal Designs retained 1 year)
  → file PNG + **JPG copy** in the goal's `files/`; **two variants** (A = the
  film's own frame, B = concept/generated) for the owner to pick at upload.
- **The proof run (2026-11-13, SH-20261111-nvidia-alone):** 3 variants built in
  the editor and verified on the downloaded files — dimensions, ≤2 MB, the 10%
  zoom test. B (the film's red-plunge frame) is clean and filed ready. Lessons
  written into the skill as blocking rules: **text ≤85% of canvas width** (A
  and C stretched edge-to-edge and clipped letters), a **PNG can exceed
  YouTube's 2 MB limit** (A: 2.19 MB — the JPG copy is the upload file), and
  placing an AI generation **auto-resizes the canvas** (C landed at 768×1344 —
  resize back via Settings and re-check margins). **No watermark** on generated
  output (checked full-frame + zoomed corner).
- **Editor quirks documented** in `references/artistly-ui-map.md` and the skill:
  Width/Height fields overwrite each other (Height first, verify before
  Create), the Images-panel Upload may expose no file input (Custom Character
  panel input is the fallback), text-box Duplicate is unreliable (fresh heading
  per line), side-handle drags stretch glyphs, no text outline/shadow control
  (legibility comes from frame choice or a dark Shape behind the text), stale
  font-size readouts, ~20–30 s Create/Save latency (~10–15 min per finished
  thumbnail once the route is known).
- **Wiring:** business-stories SKILL router gains a Thumbnails row; the
  thumbnail-brief template names the skill as its execution step; PLAYBOOK §10's
  handoff now requires two finished variants filed with the pack; filmcraft
  finishing's packaging-triangle note points at the skill. Prompt v1.16. The
  skill also lives as a working custom skill in the owner's Muse environment;
  the studio repo (public package) is not touched by this release.

## v1.15 — 2026-11-11
- **Sync of the studio repo's v1.2.0 bundle (owner order, 2026-11-11).** The
  public prompt package (`ledger-films-studio` v1.2.0, commit ece851b) received
  these updates on 2026-11-11; this release brings the same bundle into the
  internal full system, so the two repos no longer diverge on them.
- **The CONTEXT STANDARD is now channel law.** New filmcraft reference
  `skills/ledgerfilms-filmcraft/references/context-standard.md` (the working
  copy, verbatim) + a blocking **Context gate** in the filmcraft SKILL (muted,
  any 5 lines: WHAT / WHERE in the system / HOW does it work), context structure
  and context rules in PLAYBOOK §§3–4, the gate in SYSTEM_PROMPT /
  SYSTEM-PROMPT / README Step 1A, PROMPT_COMPACT, the business-stories skill's
  always-on rules, the QC checklist and fact-check-qc, and a troubleshooting
  row. Source: the owner rated the finished AI Sell-Off long-form **5/10 —
  “still lack of context”** (2026-11-09) against his benchmark, FactZaara's
  “How Crude Oil Travels From the Ocean Floor to a Giant Tanker Ship” (17M
  views; ~150-shot analysis): the gap was not pace (5.1 s/clip vs 5.6 s/shot)
  but literal referents, hidden mechanisms shown as diagrams, a system-map
  opener, tour-guide narration (one fact per line, signposts, everyday
  analogies), human anchors shown, and viewer's-life bookends. Symbolic
  tableaux + figure overlays are a patch over context, not context.
- **THE SINGLE-VOICE RULE, named (owner correction, 2026-11-07).** The AI
  Sell-Off Short v1 shipped with **doubled narration** — the video model voiced
  the line pasted into the video prompt under the clip's voiceover. Rule: the
  video prompt is **visuals-only** (no narration line, no quoted speech, no
  “narrator says”); **“Video Only (No Sound)” stays OFF** (ticking it killed
  ALL audio including the voiceover on the repair run — the visuals-only
  prompt is the kill switch); a **tail listen** on every clip is now part of
  voice verification, because doubling passes a words-present-and-in-order
  check. Written into PLAYBOOK §8, narration-and-sound, the UI map,
  PROMPT_COMPACT, the SYSTEM_PROMPT/README fallback essentials, the
  business-stories skill, fact-check-qc, the QC checklist and troubleshooting.
- **THE 600-SECOND EXPORT CAP + the verify-the-export law (learned
  2026-11-08).** VideoExpress exports cut at exactly 600.00 s and silently
  drop the end — the AI Sell-Off long-form lost its closing line and was
  finished by splicing clip 119 back at the measured boundary. Rule: trim to
  ≤600 s before export or export in parts and splice; **verify the exported
  file itself** — play start/middle/end (picture, narration, sync, closing
  line present), **head-frame sample on every clip** (clip 38 once opened on
  ~2.5 s of black and segment checks missed it), **contact-sheet scan** for
  repeated visuals (the CVS Short was rejected for repeated clips/images
  after a sync-only check passed it), tail listen per clip. Existence and
  file size are not verification. Written into PLAYBOOK §10, the UI map,
  both workflows, fact-check-qc, the QC checklist, troubleshooting and the
  SYSTEM_PROMPT/README fallback essentials.
- **Filmcraft catches up with the working copy (2026-11-07 + 2026-11-11
  corrections that had only landed in the owner's custom skills):**
  cinematography gains the **Data & context discipline** section (motif
  ration ~⅓, human-scale ground within any 3 clips, ≥4 camera behaviours /
  ≥3 angles per 10 shots, data lines shot as graphics); motion-graphics gains
  **the figure rule** (every load-bearing figure gets a planned GRAPHIC beat;
  garbled digits = shapes-only in-clip + timed editor overlay); screenplay's
  pronunciation list gains the **proven locked-voice respellings** from
  SH-20261111-nvidia-alone — “Nvidia” → **“Nuhvidia”**, “US” → **“U. S.”**,
  “Huang” unpronounceable in five spellings (reword the line to drop the
  name); filmcraft step 3 now carries the DURATION RULE parenthetical. The
  repo filmcraft tree is byte-identical to the working copy except its
  repo-relative stack path. The production-stack skill's filmcraft reference
  list now includes context-standard.
- **Re-affirmed, unchanged:** Creative mode **OFF** everywhere (already
  correct in this repo — verified by sweep), the per-clip voiceover route
  (v1.13), the DURATION RULE (v1.14), proof segment 60–90 s. PLAYBOOK title
  tag (stale at v1.3) corrected. Prompt v1.15.

## v1.14 — 2026-11-04
- **The DURATION RULE, named and blocking (owner restated: “Mind it — video
  duration depends on voiceover runtime”).** It was implicit in v1.13; now it is
  stated as a rule in PLAYBOOK §6 (boxed, above the coverage math) and §7 (no
  Manual Video Length on a narrated clip at all — its length is whatever its
  voiceover runs), the SYSTEM_PROMPT/README fallback essentials, PROMPT_COMPACT,
  the filmcraft capabilities reference, and the production-stack delegation
  block. Consequences written down where fixed numbers could have overridden
  the voice: `[ACTION]` totals and SHOT timings in the multishot format and the
  prompt-pack template are estimates **derived from the clip's voiceover line**
  (seconds allocated by the words in each shot; the generated runtime overrides
  them at the edit); pacing no longer describes a generation as a fixed 8–12 s;
  the storyboard's Planned s column is labelled a word-based voiceover estimate
  that the actual runtime replaces. Prompt v1.14.

## v1.13 — 2026-11-04
- **Voiceover is now made WITH each clip (owner directive, supersedes the v1.5
  standalone route).** The owner corrected the workflow: “You are making voiceover
  separately. I want you to make voiceover with each clip from the voiceover
  option” — in VideoExpress every generation shows a **video prompt** and an
  **audio / voiceover prompt** for that clip. Now: the visual goes in the video
  prompt, that clip's exact AUDIO line goes in the voiceover field with the locked
  channel voice (Emotion Andrew Multilingual, speed 1, pitch 0), and the clip is
  generated with its voiceover on it — **clip length follows the voiceover
  automatically**. Retired everywhere: standalone Import Media → Text to Speech
  chunks (≤1,000 chars), My AI Audio narration assets, the separate narration
  track, chunk ordering, and measuring a separate narration total. Beats are sized
  to the voiceover field (plan ≤~20 words / ≤120 characters per clip, verify the
  dialog's current limit on the first clip, split longer lines across two beats).
  The §9 gate is rewritten as count + voice-per-clip + runtime-range: a clip that
  is silent, truncated, wrong-voice or wrong-line does not count and is
  regenerated. This designs out the Anthropic failure (voiceover displaced past
  the picture on a separate track). Synced across PLAYBOOK §§6–9, SYSTEM_PROMPT /
  SYSTEM-PROMPT / README / PROMPT_COMPACT, both workflows, the business-stories
  skill + its narration / UI-map / pacing / QC / multishot references, filmcraft
  (SKILL, capabilities, screenplay, finishing, editing), the production-stack
  delegation block, storyboard / prompt-pack / QC templates, troubleshooting and
  source-map. Prompt v1.13.

## v1.12 — 2026-11-03
- **Owner correction from the Anthropic run, written into the rules:** the Manual
  Video Length control exists **only with Advanced Mode ticked ON** — with it off,
  the generation dialog shows no length control and clips default to ~5 s (all 58
  clips of LF-20261103-anthropic-ipo measured ~5 s, failing the §9 gate against
  397 s of narration; repaired with second-angle clips). PLAYBOOK §7 now requires
  Advanced Mode ON for length-critical generations (enhancement OFF, length = the
  beat's measured narration seconds), and the filmcraft capabilities reference
  carries the same rule. Also recorded (owner): when a clip's voiceover is
  generated *with* the video, its length follows the voiceover playtime
  automatically — a distinct route from the channel's standalone TTS.

## v1.11 — 2026-11-03
- **The finishing layer (owner-approved gap audit).** Filmcraft gains
  `references/finishing.md`: score & designed effects planned in the screenplay
  and mixed to ≈−14 LUFS under the narration; narration performance direction
  (pauses/emphasis marks in the AUDIO column + a pronunciation respelling list,
  also added to screenplay.md); grade shot-matching and a no-black/frozen-frame
  sweep of the finished cut; corrected captions (SRT long-form, burned-in
  Shorts), chapters, and the title–thumbnail–first-30-seconds packaging
  triangle; **YouTube AI-content disclosure ticked at upload (blocking)**; and
  the retention loop (hook ≤5 s, pattern interrupt every ~20–30 s, retention +
  CTR review at ~72 h and ~7 d with one dated lesson written back). Filmcraft
  workflow gains step 8 (finishing, mandatory); the production-stack skill
  gains an “After export” section; `templates/upload-metadata.md` gains the
  finishing checklist. Prompt v1.11; synced into SYSTEM-PROMPT.md (mirror) and
  the README copy-paste block.

## v1.10 — 2026-11-03
- **Speed discipline (owner's rule: fast execution, no wasted time).** An audit
  found no explicit speed instructions anywhere in the repo — the rule lived
  only in the owner's Muse memory from the 2026-11-03 01:10 correction (a
  finished on-site task left idle while the agent waited). Now written into the
  production-stack skill as a named section — no idle waiting (prepare the next
  step while renders run), batch to the visible queue limit, verify only at
  segment checkpoints, chase every finish into the next step in the same
  session, change tactic after the same failure twice, report measured totals
  at segment boundaries, proof-segment gate as the fail-fast rule — and into
  SYSTEM_PROMPT Step 1A item 4 plus the fallback essentials (WORK FAST line).
  Prompt v1.10; synced into SYSTEM-PROMPT.md (mirror) and the README block.

## v1.9 — 2026-11-03
- **Professional editing standard + the EDIT PASS command (owner's directives).**
  Story must follow the topic, cinematography must follow the script & voiceover,
  and the film must be multi-angle cinema — never a single zoom-in/zoom-out style.
  Filmcraft gains: `references/editing.md` (cut on the idea; every sequence
  covered from ≥3 angles/sizes; ≥4 camera behaviours in any 10 shots; zoom
  removed from the movement vocabulary — dolly/push or a cut to a closer size
  instead; sound bridges; the six-step EDIT PASS), a topic-fidelity section in
  story-structure.md (beat sheet states the topic's central question; off-topic
  beats are cut), new blocking gates in SKILL.md (topic gate, camera-serves-the-
  line rule, editing gate) and a mandatory editing pass as workflow step 7.
  SYSTEM_PROMPT Step 1A now names the editing reference and the EDIT PASS —
  which the owner can also invoke at any time with the words "Edit pass" — and
  the fallback essentials carry the multi-angle rule. Prompt v1.9; synced into
  SYSTEM-PROMPT.md (mirror) and the README copy-paste block.

## v1.8 — 2026-11-03
- **The bound stack — fixes the slideshow failure.** The Reddit long-form was
  rejected by the owner: an essay script with thematic prompts matched afterwards
  produced scenes with zero correlation to the narration (screenplay rated 1/10),
  and the VideoExpress Scripting method had been used shallowly (single-shot
  prompts; multi-shot, start-image-first and chaining mechanics unused). Now:
  new `skills/ledgerfilms-filmcraft/` (creative law — two-column AV screenplay,
  cinematography, story structure, motion graphics, VideoExpress capabilities
  checked against the upstream scripting changelog v2.6.0, blocking QC gates,
  proof-segment-first) and `skills/ledgerfilms-production-stack/` (the binding:
  one mandatory load order — Playbook → Filmcraft → Scripting adaptation →
  Production mechanics — a truthful STACK check line before any scripting or
  generation, stop-and-report if a layer is missing, and a verbatim delegation
  block for sub/browser agents). SYSTEM_PROMPT Step 1A rewritten from "install
  and load the two skills" to "load the bound stack (all skills, no subset)";
  prompt version bumped to v1.8; synced into SYSTEM-PROMPT.md (mirror) and the
  README copy-paste block. Upstream scripting text remains linked, never copied
  (CC BY-NC 4.0 — see LICENSE-NOTICES.md).
## v1.7 — 2026-10-31
- **Scene length follows the voiceover.** The narration is split into **beats of
  ≤10 s** (≈ ≤25 words, one idea per beat, sentence boundaries); each scene's Manual
  Video Length is set to its beat's **measured** narration duration — a 5 s line gets
  a 5 s scene, a 10 s line a 10 s scene (10 s is the dialog maximum). Scene count =
  beat count + ~10% B-roll; scene seconds sum to the narration total by construction.
  Replaces the fixed ⌈÷9⌉ planning average across PLAYBOOK §6, the storyboard
  template, long-form workflow, pacing-and-trim, videoexpress-ui-map,
  PROMPT_COMPACT, SYSTEM_PROMPT and README.

## v1.6 — 2026-10-30
- **Trending topics: user picks.** When the run starts with Topic = Trending (or no
  topic), the agent now researches live signals, scores the candidates, and presents
  the **top 5 as a rated slate — then STOPS**. Production starts only after the user
  chooses one (a recommendation ★ is allowed; proceeding unpicked is not). Updated
  PLAYBOOK §1A, trend-research skill §3, templates/trend-brief.md (Pick → User's
  choice) and templates/intake.md.
- **Clip duration up to 10 s.** Manual Video Length supports the full 10 s; scene
  planning should use it where the beat allows (more story per generation). Coverage
  math keeps ⌈÷9⌉ as the conservative average, with ⌈÷10⌉ noted for all-10 s plans
  (600 s → 60 minimum, plan ~66). Updated PLAYBOOK §6/§7, pacing-and-trim,
  videoexpress-ui-map, PROMPT_COMPACT.
- **Sound production aligned with the two upstream reference repos**
  (realistic-mini-dramas, videoexpress-two-character-agent): every clip is generated
  WITH the production sound described in its prompt — transient, action-tied ambience
  and effects, no dialogue, no music — never silent video. At assembly the clip
  production sound stays in the mix, **ducked low under the narration** (replaces the
  hard "muted" rule). Updated PLAYBOOK §8, narration-and-sound, fact-check-qc,
  source-map, SYSTEM_PROMPT/SYSTEM-PROMPT/README fallbacks, PROMPT_COMPACT.

## v1.5 — 2026-10-30
- **Narration route fixed (field-tested):** the generation dialog's "Narration Video"
  flow cannot build a long voice-over — it requires a generated start image, caps its
  text box at 120 characters, and each Import Speech replaces the pending audio (closing
  the dialog loses it). The channel route is now the standalone **Import Media → Text
  to Speech** panel: 2,400-char counter but a practical ~1,100-character cap (imports
  above it fail silently — 2,326 chars failed; 699/1,074 chars succeeded), so narration
  ships as **≤1,000-character sentence-boundary chunks**. Every import persists in
  **My AI Audio** labelled by its opening words with a `/library/download/<id>` link —
  record asset IDs per chunk in script order. PLAYBOOK §7.1/§8/§9, SYSTEM_PROMPT(v1.5),
  SYSTEM-PROMPT mirror, PROMPT_COMPACT, docs/source-map, narration-and-sound and
  videoexpress-ui-map references updated.
- **Timeline mechanics documented:** library assets (video and narration audio) are
  added by drag-and-drop only; drops aimed below the visible track area land nowhere —
  raise the viewport height or close the media panel; a track header's bin deletes the
  whole track row (page reload restores the default two-track layout); the Delete key
  is unreliable on clips. Added to PLAYBOOK §9 and docs/troubleshooting.md.

## v1.4 — 2026-10-29
- **Footage-coverage gate (blocking) — fixes the Dollar General underrun.** The first
  Dollar General export had ~2:42 of picture against 7:24 of narration: 30 scenes had
  been planned as if they could cover a long-form, and no step compared measured
  footage seconds with measured narration seconds before export. Now:
  PLAYBOOK (v1.3) §6 adds mandatory **coverage math** — VideoExpress clips are 8–10 s,
  generations needed = ⌈ narration seconds ÷ 9 ⌉ + ~10% safety (444 s → ~55 planned;
  600 s → ~74), every clip's **measured** duration is recorded with a running total,
  and a route returning ~5 s clips forces a re-count at the measured length.
  §7 adds duration discipline, §8 requires measuring the locked narration (chunk
  totals summed), **§9 adds a ⛔ blocking underrun gate** — video total <
  narration total − 2 s means STOP: no final save, no export, no "finished" report;
  generate more coverage and reassemble; frozen/black/looped/slowed filler is not
  coverage. §10 handoff must state both measured totals and confirm the gate passed.
  Synced into `workflows/long-form-16x9.md`, `templates/qc-checklist.md`,
  `templates/storyboard-long-form.md`, `templates/prompt-pack.md`,
  `skills/ledgerfilms-business-stories/references/pacing-and-trim.md` and
  `fact-check-qc.md`, `PROMPT_COMPACT.md`, and the fallback essentials in
  `SYSTEM_PROMPT.md` / `SYSTEM-PROMPT.md` / README copy-paste block.

## v1.3 — 2026-10-27
- SYSTEM_PROMPT: new **Step 1A — Install and load the two skills**, between loading
  the playbook and following it. Trend-research skill: loaded from this repo (no
  install) and used at start (Trending / no topic / Full week), as a light pass for
  user topics, and at export for the keyword & hashtag pack. VideoExpress Scripting
  skill: agent checks whether the upstream `ratava/videoexpress-scripting-skill` is
  installed, gives the user the Claude Desktop / ChatGPT marketplace install steps
  and waits if it isn't, falls back to this repo's `SKILL-ADAPTATION.md` + PLAYBOOK
  §6 when installation isn't possible, and must flag the upstream skill's
  CC BY-NC 4.0 licence before relying on it for the monetised channel. Step 2 now
  names the scripting skill at prompt-pack stage. Synced to `SYSTEM-PROMPT.md`
  (mirror) and the README copy-paste block; prompt version bumped to v1.3.

## v1.2 — 2026-10-27
- **New skill: `skills/ledgerfilms-trend-research/`** — finds a real hot topic from
  live signals instead of model memory. Sources: Google Trends, YouTube (search,
  autocomplete, trending), Reddit, business news and earnings/event calendars, plus
  supporting signals (TikTok/Reels search, X, Wikipedia pageviews). References cover
  the source/signal method, a 10-factor /50 hot-topic scoring rubric with publish-by
  windows, and a per-platform keyword & hashtag guide.
- Wired into production start: PLAYBOOK §1A runs the skill when Topic is `Trending`
  or blank, before a Full-week slate, or when the user asks what's hot; a user-given
  topic gets the light pass only. `templates/trend-brief.md` added for the ranked
  slate; intake and upload-metadata templates gained topic-source and keyword/hashtag
  fields; PLAYBOOK §10 handoff now requires the keyword & hashtag pack for YouTube
  long-form, YouTube Shorts, TikTok, Instagram Reels, Facebook and X.
- SYSTEM_PROMPT bumped to v1.2 (mirrored in `SYSTEM-PROMPT.md` and the README
  copy-paste block): Step 0 offers Topic = `Trending`, Step 2 runs §1A first.

## v1.1 — 2026-10-26
- `SYSTEM_PROMPT.md` is now the canonical, paste-ready prompt (full text, modelled on the
  upstream `realistic-mini-dramas` SYSTEM_PROMPT layout), with `SYSTEM-PROMPT.md` kept as
  a mirror for existing links. Step 1 now loads `PLAYBOOK.md` from this repo's own GitHub
  URLs (raw, with the blob page as fallback). Added the browser/process-error recovery
  note (re-show the Step 0 Full-access note, then resume) and a self-contained fallback
  essentials block for when GitHub won't load at all.
- Noted in the prompt that this repo is private, so GitHub may ask for a sign-in in
  Step 1 (the upstream playbook is public; this one is not).

## v1.0 — 2026-10-26
- Initial LedgerFilms restructure. Merged the documentary spine of
  `historical-documentary-video-workflow`, the pacing/trim and repo structure of
  `realistic-mini-dramas`, and the narration/continuity/queue rules of
  `videoexpress-stickman-story-agent` into one playbook for AI-illustrated business &
  money stories.
- Two formats locked: long-form ~10 min 16:9; Shorts 45–60 s 9:16. Weekly cadence
  1 + 4 inside a 15-hour production budget.
- Added: two-source fact-check and legal rules, Founder & Company Bible, topic bank
  (30 scored topics), week-01 sample calendar, worked examples, QC checklist.
- VideoExpress Scripting skill referenced, not vendored — CC BY-NC 4.0 (see
  `LICENSE-NOTICES.md`).
