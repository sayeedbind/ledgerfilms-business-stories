# Changelog

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
