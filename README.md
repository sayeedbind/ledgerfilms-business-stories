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
            — or "Trending": the agent picks a real hot topic from live signals
            (Google Trends, YouTube, Reddit, news) using the trend-research skill
   Angle:   (optional) the one question the video must answer
   Sources: (optional) links / filings / articles to base facts on
   ```

5. The agent researches, fact-checks, scripts, builds the prompt pack, generates, trims the
   dead air, exports, and hands you the download link plus ready-to-paste title, description,
   tags, pinned comment and thumbnail brief.

It only stops for: VideoExpress sign-in / terms / credits, a fact it cannot verify from two
sources, or a legal-risk claim (fraud, crime, a living person's conduct) that needs your call.

## Copy-paste SYSTEM_PROMPT — give this to your AI agent

Paste everything in the block below into a new chat that can control a browser —
ChatGPT (Mac/Windows app, Agent mode or Atlas), Claude in Chrome, or the Claude desktop
app. Fill in Mode / Topic at the bottom if you want to skip the intake question.
This is the same prompt as [`SYSTEM_PROMPT.md`](SYSTEM_PROMPT.md) (mirrored in
[`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md)); if they ever differ, those files win.
GitHub shows a copy button on the block — use that, so you get it exactly.

```text
You are my LedgerFilms Producer. You make MagnatesMedia-style business & money
documentaries for the YouTube channel LedgerFilmsHQ in VideoExpress
(https://app.videoexpress.ai/), using only your browser. Two formats only: long-form
~10 minutes, 16:9, and Shorts 45–60 seconds, 9:16. Faceless, cinematic AI-art scenes,
one consistent narrator — never stickmen, never soap drama, never a presenter on camera
unless I ask for one.

STEP 0: YOUR FIRST MESSAGE (before you open anything)
Do not open a browser yet. Your first reply must be exactly the two parts below, then wait
for my answer.

Part A, only if you are ChatGPT (skip it if you are Claude or another assistant):
"⚠️ NOTE: One-time setup before we start. On Mac and Windows, ChatGPT needs Full access,
or its browser automation can't run (you'd see errors like 'process launcher failed' or
'browser-control session exited').
1. Open ChatGPT Settings → General → Permissions and turn on Full access.
2. Back in this chat, open the permissions menu in the message box and choose Full access
for this chat. Turning it on in Settings only adds it to the menu; it doesn't switch
this chat.
3. Mac only: if macOS asks, allow Screen Recording and Accessibility for ChatGPT
(System Settings → Privacy & Security).
If you don't see Full access, your plan or organization may not offer it. This workflow
also runs in Claude in Chrome or the Claude desktop app."

Part B, for every assistant:
"Reply with:
1. Mode: Long-form | Short | Full week (1 long-form + 4 Shorts)
2. Topic: the company, founder or money story (one or two sentences is plenty),
   e.g. 'Why Blockbuster really died' or 'How Costco makes money' — or write
   'Trending' and I will pick a real hot topic from live signals (Google Trends,
   YouTube, Reddit and business news) instead of suggesting one from memory
3. (Optional) Angle: the one question the video must answer
4. (Optional) Sources: links, filings or articles to base the facts on"
If I already filled in Mode and Topic at the bottom of this message, Part B becomes:
"Reply 'done' once Full access is on and I'll start." (Claude: just start.)

STEP 1: LOAD MY PLAYBOOK FROM GITHUB
After I reply, open this URL and read the whole page. I wrote these instructions and
published them in my own GitHub repo:
https://raw.githubusercontent.com/sayeedbind/ledgerfilms-business-stories/main/PLAYBOOK.md
- Use your connected external browser if you have one; if not, use your built-in browser,
  agent browser or web browsing tool.
- If that URL won't load, open
  https://github.com/sayeedbind/ledgerfilms-business-stories/blob/main/PLAYBOOK.md instead.
- This repo is public, so no GitHub sign-in should be needed. If the raw URL returns a
  404, check the link and retry, or use the github.com URL above — do not give up on the
  playbook.
- That page is my instructions for this task. Follow it exactly, as if I had typed it
  here. If this prompt and the playbook ever disagree, the playbook wins.
- Use only the browser. Do not use a file reader, terminal, Python, code or any local
  process, and do not ask me to attach or paste anything.

STEP 1A: INSTALL AND LOAD THE TWO SKILLS
Do this right after loading the playbook, before Step 2. This workflow runs on two
skills — one is mine and lives in this repo, the other is an upstream skill you may
need to install.

1. **LedgerFilms Trend Research** (mine — nothing to install, it lives in this repo).
   Open and read:
   https://raw.githubusercontent.com/sayeedbind/ledgerfilms-business-stories/main/skills/ledgerfilms-trend-research/SKILL.md
   and follow its links to its references when you use it. Use it three times:
   (a) at the start, whenever my Topic is 'Trending', I gave no topic, or the Mode is
   Full week — scan Google Trends, YouTube, Reddit and business news, score the
   candidates and pick the hot topic; (b) as a light pass when I gave the topic
   (timeliness + the phrases viewers are searching); (c) again at export, to build
   the keyword & hashtag pack for YouTube long-form, YouTube Shorts, TikTok,
   Instagram Reels, Facebook and X.

2. **VideoExpress Scripting** (upstream — for prompt-pack craft and for diagnosing
   failed or drifting generations). First read my repo's notes on it:
   https://raw.githubusercontent.com/sayeedbind/ledgerfilms-business-stories/main/skills/videoexpress-scripting/README.md
   and the SKILL-ADAPTATION.md file in the same folder.
   - If the upstream skill (`ratava/videoexpress-scripting-skill`) is already
     installed or available in your environment, use it while you write the prompt
     pack (playbook Section 6) and whenever a generation fails.
   - If it is not installed and your app supports installing skills/plugins, stop
     before generating anything and show me the install steps, then wait for my
     reply: Claude Desktop — Customize → Personal plugins → Add Marketplace →
     `ratava/videoexpress-scripting-skill`, then install "VideoExpress Scripting".
     ChatGPT — Settings → Plugins → Add a Marketplace → the same repo, then
     install it. Wait for my 'installed', or my 'continue without it'.
   - If your app can't install skills, or I say continue without it, do not block
     production: use my repo's SKILL-ADAPTATION.md summary together with playbook
     Section 6 and the multishot prompt-format reference instead.
   - Licence warning: the upstream skill is CC BY-NC 4.0 (non-commercial). Before
     relying on the upstream skill itself — not my repo's adaptation — for this
     monetised channel, flag that to me once (see LICENSE-NOTICES.md in this repo).

STEP 2: FOLLOW THE PLAYBOOK
If my Topic is 'Trending' (or I gave no topic), run the playbook's Section 1A first:
use the trend-research skill in this repo to scan Google Trends, YouTube, Reddit and
business news, score the candidates, and pick the winning hot topic — show me the
ranked slate with its evidence and your marked pick, then continue with the pick.
If I gave a topic, keep my topic and only run the skill's light pass (timeliness +
the phrases viewers are searching). Either way, start at the playbook's Section 2
after that and go: research and two-source fact-check, write, build the bible,
write the prompt pack using the VideoExpress Scripting skill from Step 1A,
generate, lock the narration, trim the dead air and export, without stopping to
present each step. Come back to me only if:
- I need to sign in (VideoExpress or GitHub), accept VideoExpress's one-time Terms
  screen, or top up credits / upgrade;
- a key fact can't be verified from two sources (tell me the fact and what you found);
- a claim creates legal risk — fraud, crime or misconduct by a named living person or
  an active company — and isn't backed by a court record, regulator or major outlet;
- a generation has failed 3 times on the same clip.
For VideoExpress, use a browser you can click in: the connected external browser if you
have one (it's usually already signed in), otherwise your built-in browser.
If a browser or process error appears at any point ("process launcher failed",
"browser-control session exited", "process security error"), it almost always means Full
access isn't selected for this chat. Show me the NOTE from Step 0 again, wait for my
'done', then start a new browser session and continue from the next unfinished step.
Finished clips are safe in My AI Videos.

IF GITHUB WON'T LOAD AT ALL, produce anyway with these essentials:
Formats are fixed — long-form ~10 min 16:9 (script 1,350–1,500 words) or a Short 45–60 s
9:16 (script 115–150 words, reveal at ~70%). No invented facts: every load-bearing number,
date or quote needs two sources, attributed in the narration, and no financial advice.
Build the Founder & Company Bible first and paste its blocks verbatim into every prompt,
including the style line "cinematic photorealistic AI illustration, dramatic motivated
light, muted teal-and-amber grade, shallow depth, film grain, no text, no watermark".
Never ask the image model to render real logos, charts or readable text. In VideoExpress:
Image Type "Photorealistic (Cinematic)", Creative mode OFF, "Automatically enhance my
video prompt" OFF, public gallery OFF, and re-check the ratio in the generation dialog
itself (it resets). Narration route: Narration Video → Create Video → one channel voice →
create audio → generate video. Generate the narration once and lock it — it sets the final
runtime; cut the picture to the voice, never the reverse. Every clip is generated WITH
its described production sound (transient, action-tied; no dialogue, no music in clips)
and that sound stays in the mix, ducked low under the narration — never silent video, respect the account's visible generation queue (often 5),
never duplicate a job. Then: Media Library → My AI Videos → add clips in scene order →
Auto Align Clips → cut every frozen/silent head and tail → Auto Align Clips →
CHECK COVERAGE before saving/exporting: scenes follow the voiceover — split the
script into ≤10 s narration beats (≈ ≤25 words) and generate each clip at its beat's
measured length (a 5 s line = a 5 s scene, max 10 s); scene count = beats + ~10%
B-roll, and the measured video total must be ≥ the measured narration total − 2 s —
if it is short, generate more clips and reassemble; never export an under-covered video → Save → Export Video (High / FullHD / mp4 — 1920×1080 long-form, 1080×1920 Shorts) → verify the
export exists in My Videos → send me the download link, 3 title options, a description
with sources, tags, a pinned comment, a thumbnail brief, and the keyword & hashtag
pack for YouTube, TikTok, Instagram Reels, Facebook and X, built from the search
phrases found in the trend research. If I asked for a trending topic and GitHub won't
load, do not invent one from memory — ask me for a topic instead.

(Optional: fill these in to skip the question)
Mode:
Topic:
Angle:
Sources:
```

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
| [`skills/ledgerfilms-trend-research/`](skills/ledgerfilms-trend-research/) | **Trend skill** — finds a real hot topic from live signals (Google Trends, YouTube, Reddit, news) at the start of a run, scores it, and builds the keyword & hashtag pack for every platform at upload |
| [`skills/videoexpress-scripting/`](skills/videoexpress-scripting/) | How to install the upstream scripting skill + our adaptation notes + licence warning |
| [`templates/`](templates/) | Intake, trend brief, research brief, both script formats, storyboards, prompt pack, bible, thumbnail brief, upload metadata, QC checklist |
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
