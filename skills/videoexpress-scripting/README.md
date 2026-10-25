# Upstream skill: VideoExpress Scripting (install, don't copy)

**Repo:** https://github.com/ratava/videoexpress-scripting-skill (v2.5.6 at time of writing)
**What it is:** an Agent Skill for planning/scripting multi-clip VideoExpress videos —
guided intake, Core Bible, multishot prompt format, 45+ style sheets, chaining rules,
failure-mode fixes, and a browser workflow for driving VideoExpress.
**Licence: CC BY-NC 4.0** (© Brent Wesley) — **NonCommercial.** ⚠️ Read
`../../LICENSE-NOTICES.md` before using it in monetised LedgerFilms production.

## Install (upstream routes, per its README)
- **Claude Desktop:** Customize → Personal plugins → Add Marketplace →
  `ratava/videoexpress-scripting-skill`, then install *VideoExpress Scripting*.
- **ChatGPT:** Settings → Plugins → Add a Marketplace → same repo.
- **Grok:** ask it to install from the repo's `chatgpt/skills/videoexpress-scripting` folder.
- It also ships a companion single-prompt wizard, *VideoExpress Prompt*
  (`claude-prompt/` / `chatgpt-prompt/` folders upstream).

## How LedgerFilms uses it
- As a **craft reference** for prompt packs and failure diagnosis, behind our own
  PLAYBOOK — where the two disagree on channel matters (style, formats, facts), PLAYBOOK wins.
- Our original-wording summary of the method lives in `SKILL-ADAPTATION.md` and in
  `../ledgerfilms-business-stories/references/multishot-prompt-format.md`.
- Nothing from that repo is vendored into this one. If you obtain a commercial licence
  from the author, note it here with the date and scope.
