# Changelog

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
