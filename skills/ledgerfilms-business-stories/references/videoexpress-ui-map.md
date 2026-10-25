# VideoExpress UI map (as used by the merged workflows)

*Operational notes distilled from the three upstream playbooks. VideoExpress changes its
UI — if a label differs, follow the PLAYBOOK's intent and note the change in the repo.*

- **Create a scene:** create image first (with Consistent Character reference slots:
  Ref 1 = character master, Ref 2 = location/environment master where supported),
  then create video from that image.
- **Style routing (channel look):** Image Type **Photorealistic (Cinematic)**,
  Creative mode **off**. The LedgerFilms style line travels inside the prompt text.
- **Narration route:** Narration Video → Create Video → CloneVoice / System Voice →
  pick the channel narrator → create audio → generate video. Advanced Mode off for this
  route in the stickman-derived workflow; for documentary multi-shot clips, Advanced Mode
  may be on with **automatic enhancement OFF** and **Manual Video Length ON**.
- **The dialog trap:** before EVERY submission, check the settings *inside the generation
  dialog* — its ratio selector can reset to 9:16 and prompt-enhancement can re-tick after
  a re-render, independently of the project bar. Fix only what reset; keep references.
- **Parallel renders:** up to 5 concurrent video jobs on many accounts — the visible
  account limit is the rule. A full queue is a wait state, not an error.
- **Assembly:** Media Library → My Media → My AI Videos → right-click a completed clip →
  Add to Timeline; confirm one clip landed before adding the next.
- **Trim:** timeline zoom ~40 px/s; Cut + Delete for frozen/silent heads and tails;
  **Auto Align Clips** to close gaps.
- **Export:** High quality / FullHD / MP4 — 1920×1080 (16:9) or 1080×1920 (9:16).
  Exports live in **My Videos** (upstream notes a 40-day window) — download same day.
- **Always:** public gallery / sharing OFF, "Automatically enhance my video prompt" OFF,
  no music generated into clips.
