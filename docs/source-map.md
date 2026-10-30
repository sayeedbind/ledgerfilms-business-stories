# Source map — what came from where, and what was changed

Checked against the live repos on 2026-10-26. This file is the audit trail for the merge.

## 1. ai-playbooks/realistic-mini-dramas — the template
**Kept as the structural model:** root layout (README, SYSTEM_PROMPT, PLAYBOOK,
PROMPT_COMPACT, CHATGPT_SETUP, AGENTS/CLAUDE, examples/, skills/, docs/, assets/),
the "short prompt loads a full playbook" pattern, and the production mechanics:
hook-first script, ~3 s per shot, Character Bible + Consistent Character, image-first
generation, Photorealistic (Cinematic) style routing, clips on track 1 + Auto Align,
**dead-air trim** at ~40 px/s, FullHD export, 5-parallel render note, 40-day export window.
**Changed:** 9:16-only soap drama → one of two formats; romance/revenge plots → business
stories; the 70% "twist" → the 70% **reveal of the money mechanism**; dialogue-led scenes →
narration-led scenes (no acting dialogue); its 45 s default → 45–60 s Short spec.

## 2. ai-playbooks/historical-documentary-video-workflow — the documentary spine
**Kept:** the core premise "the history of a subject **and how it was built**" (→ how the
company / fortune / market was built); narration generated once, never re-cut or
speed-changed, with the final runtime following the audio; timed multi-shot clips
(SHOT 1/2/3, hard cuts, distinct angles, connected physical actions); period accuracy of
clothing, tools and architecture (→ era block); scene audio muted under narration;
reuse completed assets when resuming; cut only the excess video at the narration's edge.
**Changed:** watercolor-and-ink → cinematic photoreal house style; presenter intro
(≥20 s, Daniel Reed) → **dropped as default** (LedgerFilms is faceless; presenter is an
optional variant in the bible template); 60 s–5 min duration → ~10 min long-form;
CloneVoice standalone route → VideoExpress in-app narration route (from repo 3).

## 3. ai-playbooks/videoexpress-stickman-story-agent — narration & continuity ops
**Kept (revised 2026-10-30):** narration is created in VideoExpress, but via the
standalone Import Media → Text to Speech route in ≤1,000-character chunks — the
Narration Video dialog route from the stickman agent proved unusable for long
voice-overs (120-character cap, replace-per-import); design the whole sequence before generating (incoming →
action → outgoing → next-opening states); fresh start images from the master rather than
last-frame chaining by default; fixed location layouts with counts/positions that must not
drift; concurrent-slot discipline (often 5, full queue = wait, never duplicate); max
3 attempts per clip; re-checking the generation dialog's own ratio selector and
enhancement toggle before every submission; the acceptance-checklist idea (→ QC template);
"a completion badge is not proof of quality".
**Changed:** 2D stickman cast → cinematic scenes with a Founder & Company Bible; per-story
new protagonist names → per-video protagonist (founder/company) with a channel-constant
narrator; adventure-story beats → business story spine (§3 of PLAYBOOK).

## 4. ratava/videoexpress-scripting-skill — prompt craft (referenced, not copied)
**Kept as method, in original wording:** prompt-pack discipline, Core Bible pasted
verbatim, the multishot section format, "the model renders nouns, not intentions",
positives-except-in-[NEGATIVES], quotes-mean-speech, camera moves need destinations,
~6,000-character prompt box, auto-enhance off, failure-fix-by-mechanism.
**Not taken:** any of its files or text — it is **CC BY-NC 4.0**, which conflicts with a
monetised channel. Install it upstream for study; see `LICENSE-NOTICES.md` and
`skills/videoexpress-scripting/SKILL-ADAPTATION.md`.

## 5. The reference SYSTEM-PROMPT example
The DualUp community page for the realistic-mini-dramas workflow
(community.dualup.com/@videoexpress/workflows/realistic-mini-dramas-workflow) renders as a
JS shell and its text is the same SYSTEM_PROMPT pattern as repo 1 — STEP 0 first-message
script (Full access warning + intake), then "load PLAYBOOK.md from GitHub". Our
`SYSTEM-PROMPT.md` follows that exact pattern with LedgerFilms intake fields.
