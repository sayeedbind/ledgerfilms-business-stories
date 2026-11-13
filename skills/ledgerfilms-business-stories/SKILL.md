---
name: ledgerfilms-business-stories
description: Produce AI-illustrated business & money documentaries for the LedgerFilmsHQ YouTube channel in VideoExpress — long-form ~10 min 16:9 and Shorts 45–60 s 9:16. Covers researched and fact-checked scripts, the Founder & Company Bible, the multishot prompt pack, in-VideoExpress narration, continuity and queue discipline, dead-air trimming, export and upload packaging. Use whenever the user asks for a LedgerFilms video, a business/founder/company story video, a VideoExpress documentary or Short, or reports a production problem (character drift, wrong ratio, garbled text/numbers, era errors, narration mismatch).
---

# LedgerFilms Business Stories

Produce a finished, export-verified video — not a plan. Two formats only:
**long-form ~10:00, 16:9** and **Shorts 45–60 s, 9:16**, for English-speaking 18–45
viewers (US/UK/CA/AU). Faceless, cinematic AI art + one narrator.

The full instructions are in `../../PLAYBOOK.md` — read it before a production run.
This skill is the router and the always-on rules.

## Read next, by step
| Step | Read |
|---|---|
| Intake, formats, weekly cadence | `../../PLAYBOOK.md` §1, §4 · `../../workflows/` |
| Topic = Trending, what's hot, keywords/hashtags | `../ledgerfilms-trend-research/SKILL.md` · `../../PLAYBOOK.md` §1A |
| Research / any factual claim | `../../docs/fact-check-and-legal.md` · `references/fact-check-qc.md` |
| Bible, masters, locations | `references/bible-and-continuity.md` |
| Writing any prompt | `references/multishot-prompt-format.md` |
| Operating VideoExpress | `references/videoexpress-ui-map.md` |
| Narration (per-clip voiceover), voices, music | `references/narration-and-sound.md` |
| Pacing, trim, export gate | `references/pacing-and-trim.md` · `references/fact-check-qc.md` |
| Thumbnails & Shorts covers (Artistly) | `../ledgerfilms-thumbnails/SKILL.md` · `../../templates/thumbnail-brief.md` |

## Always-on rules
1. **No invented facts.** Two sources per load-bearing fact, one primary where possible.
2. **Bible blocks verbatim** in every prompt. Paraphrase is drift.
3. **Voiceover made WITH each clip** — that clip's line goes in the generation dialog's voiceover field, locked voice; never generate narration separately, never build a separate narration track. A bad read = regenerate that clip.
3a. **Single voice only** — the video prompt describes visuals only: never the narration line, never quoted speech (the model voices any line it is given and the narration doubles). **Video Only (No Sound) stays OFF** — ticking it kills all audio including the voiceover.
3b. **Context Standard** — every named noun shown as itself, hidden mechanisms as diagram beats, system-map opener, tour-guide narration (one fact per line), viewer's-life bookends. The filmcraft Context gate is blocking (PLAYBOOK §§3–4).
4. Ratio re-checked **inside the generation dialog**; auto-enhance OFF; gallery OFF; no music in clips.
5. Quotes mean speech — quote nothing in visual prompts; narration carries all words.
6. Never ask the model to render text, logos, charts or numbers — overlays do that later.
7. Queue honestly: parallel slots only, full queue = wait, max 3 attempts per clip.
8. Era accuracy is a QC gate, not a nicety.
9. No financial advice anywhere — script, description, comments.
10. Finish = export verified + upload pack delivered (titles, description, pinned comment, thumbnail brief). Exports are hard-capped at **600 s** — trim to ≤600 s or export in parts and splice; “verified” means the exported file itself was played (start/middle/end), head frames sampled, contact sheet scanned, tails listened to (PLAYBOOK §10).

## If the upstream VideoExpress Scripting skill is installed
Use it for prompt craft and failure diagnosis — subject to its **CC BY-NC 4.0** licence.
Flag commercial use to the user (see `../../LICENSE-NOTICES.md`) instead of silently
relying on it for a monetised channel.
