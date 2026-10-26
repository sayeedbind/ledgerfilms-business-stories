# Changelog

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
