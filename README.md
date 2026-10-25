# LedgerFilms — AI-Illustrated Business & Money Stories: VideoExpress Workflow v1.0

Paste one prompt, name a company / founder / money story, and your AI agent builds a
**MagnatesMedia-style business documentary** for [LedgerFilmsHQ](https://www.youtube.com/@LedgerFilmsHQ)
inside [VideoExpress](https://app.videoexpress.ai/): researched script, cinematic AI-art scenes,
one consistent narrator, a trimmed timeline — and **four 45–60 s Shorts cut from the same story**.

This repo merges and re-purposes three upstream playbooks, plus one scripting skill — see
[`docs/source-map.md`](docs/source-map.md) for exactly what came from where, and what changed.

| Source | What was taken | What changed for LedgerFilms |
|---|---|---|
| `ai-playbooks/realistic-mini-dramas` | Repo structure, PLAYBOOK pattern, fast pacing, dead-air trim, Character Bible | Soap drama → business story; twist → *reveal of the hidden money mechanism* |
| `ai-playbooks/historical-documentary-video-workflow` | Documentary spine: "history of X and how it was built", narration-drives-runtime, timed multi-shot clips | History subject → company / founder / market; watercolor → cinematic AI art; presenter intro → optional |
| `ai-playbooks/videoexpress-stickman-story-agent` | Narration route in VideoExpress, continuity handoffs, fixed location layouts, concurrent generation, acceptance checklist | Stickmen → cinematic scenes + consistent founder/company bible; no character dialogue by default |
| `ratava/videoexpress-scripting-skill` | Prompt-pack method, Core Bible, multishot prompt format | **Not vendored** — CC BY-NC 4.0. Linked and adapted in summary only. See [`LICENSE-NOTICES.md`](LICENSE-NOTICES.md) ⚠️ |

## The channel

- **Niche:** AI-Illustrated Business & Money Stories
- **Audience:** English-speaking, 18–45, US / UK / CA / AU — self-improvement readers and curious
  professionals. Chosen for the highest advertiser intent on YouTube: finance, business, SaaS,
  investing and productivity sponsors pay for this viewer.
- **Style:** Faceless documentary. Cinematic AI-art scenes + one narrator voice. No presenter
  on camera, no stickmen, no soap-drama characters, no on-screen acting dialogue by default.
- **Content pillars:** Rise & Fall · How They Actually Make Money · Founder Wars ·
  Collapses & Scams (sourced, legally careful) · Money Mechanics explainers.

## Weekly cadence — fits in 15 hours

| Slot | Format | Spec | Publish (ET) |
|---|---|---|---|
| 1 × long-form | Documentary | **~10 min · 16:9 · 1920×1080** | Tue 9–10 AM (Sun works too) |
| 4 × Shorts | Vertical story | **45–60 s · 9:16 · 1080×1920** | Mon / Wed / Thu / Fri, 6–9 PM |

Every upload: pinned comment in the first minutes, reply to comments for the first 60 minutes.
Shorts are not leftovers — 2 are cut from the week's long-form, 2 are standalone hooks that
tease next week's topic. Full hour-by-hour plan: [`docs/weekly-schedule-15h.md`](docs/weekly-schedule-15h.md).

## Quick start (2 minutes)

1. Sign in to [app.videoexpress.ai](https://app.videoexpress.ai/) (or sign in when the agent asks).
2. Open a **new chat that can control a browser** — ChatGPT app (set **Settings → General →
   Permissions → Full access** first, see [`CHATGPT_SETUP.md`](CHATGPT_SETUP.md)) or Claude
   (Claude in Chrome / desktop app).
3. Paste [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) — it tells the agent to load [`PLAYBOOK.md`](PLAYBOOK.md)
   from this repo and run the whole production.
4. Answer the one intake question:

   ```
   Mode:    Long-form | Short | Full week (1 long + 4 Shorts)
   Topic:   e.g. "How Costco actually makes money — and why the hot dog is still $1.50"
   Angle:   (optional) the one question the video must answer
   Sources: (optional) links / filings / articles to base facts on
   ```

5. The agent researches, fact-checks, scripts, builds the prompt pack, generates, trims the
   dead air, exports, and hands you the download link plus ready-to-paste title, description,
   tags, pinned comment and thumbnail brief.

It only stops for: VideoExpress sign-in / terms / credits, a fact it cannot verify from two
sources, or a legal-risk claim (fraud, crime, a living person's conduct) that needs your call.

## How it works

| Stage | Long-form (16:9) | Short (9:16) |
|---|---|---|
| Script | 1,350–1,500 words ≈ 10 min at documentary pace | 115–150 words = 45–60 s |
| Structure | Hook → stakes → origin → mechanism → turning point → fall/climax → lesson | Hook (0–3 s) → setup → escalation → **reveal at ~70%** → loop/CTA |
| Visuals | 60–75 clips, multi-shot generations, ~4 s per visual beat | 10–14 clips, ~3 s per shot |
| Bible | Founder + company + era + location blocks, pasted verbatim in every prompt | Same bible, vertical-safe framing (subject centre-frame) |
| Narration | One narrator, generated first; **narration sets the final runtime** | Same narrator, same settings |
| Edit | Clips on track 1, Auto Align, every frozen/silent head & tail cut | Same, tighter: no shot outlives its line |
| Export | High / FullHD 1920×1080 / MP4 | High / FullHD 1080×1920 / MP4 |

## Files

| File | Use it for |
|---|---|
| [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) | **The prompt to paste** into your AI agent |
| [`PLAYBOOK.md`](PLAYBOOK.md) | The full production instructions the agent loads and follows |
| [`PROMPT_COMPACT.md`](PROMPT_COMPACT.md) | <8,000-character version for a Custom GPT / Claude Project |
| [`workflows/`](workflows/) | Step-by-step: long-form, Shorts, and repurposing long → Shorts |
| [`skills/ledgerfilms-business-stories/`](skills/ledgerfilms-business-stories/) | Agent Skill version (SKILL.md + references: UI map, pacing/trim, multishot format, bible, narration, QC) |
| [`skills/videoexpress-scripting/`](skills/videoexpress-scripting/) | How to install the upstream scripting skill + our adaptation notes + licence warning |
| [`templates/`](templates/) | Intake, research brief, both script formats, storyboards, prompt pack, bible, thumbnail brief, upload metadata, QC checklist |
| [`examples/`](examples/) | Two complete worked examples (1 long-form, 1 Short) with prompts written out |
| [`production/topic-bank.md`](production/topic-bank.md) | 30 scored topics: 10 long-form + 20 Short hooks |
| [`production/week-01-calendar.md`](production/week-01-calendar.md) | A filled-in sample week |
| [`docs/`](docs/) | Niche & audience, 15-hour schedule, fact-check & legal, titles/thumbnails, troubleshooting, source map |
| [`AGENTS.md`](AGENTS.md) / [`CLAUDE.md`](CLAUDE.md) | Auto-loaded by Codex / Claude Code |
| [`GITHUB_UPLOAD.md`](GITHUB_UPLOAD.md) | Push this repo to your own GitHub account |

## Non-negotiables

1. **No invented numbers.** Every revenue figure, date, valuation and quote needs two sources,
   one of them primary where possible (filing, earnings call, court record, company report).
   Unverifiable = cut or flagged to you, never narrated as fact. See [`docs/fact-check-and-legal.md`](docs/fact-check-and-legal.md).
2. **Narration first, picture second.** The locked narration sets the runtime. Never speed up,
   chop or re-generate narration to hit an exact minute count.
3. **One narrator, one look.** Same voice, same cinematic art direction, same bible blocks —
   verbatim — in every clip of a video, and the same narrator across the channel.
4. **Auto-enhance OFF, public gallery OFF, no music baked into clips.** Music is added once,
   low, at the edit stage, under the narration.
5. **This is storytelling, not financial advice.** No buy/sell recommendations, no price
   predictions. Standard disclaimer in every long-form description.

## Good to know

- Each image + video generation uses VideoExpress credits. Budget roughly 60–75 video
  generations for a long-form and 10–14 per Short, plus ~15% for retries (max 3 attempts per clip).
- VideoExpress renders up to 5 videos in parallel on many accounts — the agent queues to that
  limit and never duplicates a job to "speed it up".
- AI scenes drift (a face, a logo, a period detail). The Bible + Consistent Character +
  era/location blocks keep it to a minimum; the QC checklist in `templates/qc-checklist.md`
  is the final gate before export.
- Exports stay in **My Videos** for 40 days in the upstream workflow — download and archive
  locally the same day.
