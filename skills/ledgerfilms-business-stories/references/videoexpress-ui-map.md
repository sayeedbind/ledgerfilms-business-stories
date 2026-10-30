# VideoExpress UI map (as used by the merged workflows)

*Operational notes distilled from the three upstream playbooks. VideoExpress changes its
UI — if a label differs, follow the PLAYBOOK's intent and note the change in the repo.*

- **Create a scene:** create image first (with Consistent Character reference slots:
  Ref 1 = character master, Ref 2 = location/environment master where supported),
  then create video from that image.
- **Style routing (channel look):** Image Type **Photorealistic (Cinematic)**,
  Creative mode **off**. The LedgerFilms style line travels inside the prompt text.
- **Narration route (revised 2026-10-30):** Import Media → Text to Speech — standalone
  panel with Language/Voice/Emotions/Speed/Pitch and a 2,400-char counter (practical cap
  ~1,100; use ≤1,000-char chunks). NOT the dialog's Narration Video flow: it needs a
  start image, caps at 120 characters, and replaces the pending audio per import.
  Audio assets persist in My AI Audio (label = opening words; /library/download/<id>
  links). For documentary multi-shot clips, Advanced Mode may be on with **automatic
  enhancement OFF** and **Manual Video Length ON**.
- **The dialog trap:** before EVERY submission, check the settings *inside the generation
  dialog* — its ratio selector can reset to 9:16 and prompt-enhancement can re-tick after
  a re-render, independently of the project bar. Fix only what reset; keep references.
- **Parallel renders:** up to 5 concurrent video jobs on many accounts — the visible
  account limit is the rule. A full queue is a wait state, not an error.
- **Assembly:** Media Library → My Media → My AI Videos → **drag** each completed clip
  onto the timeline (audio assets drag from My AI Audio the same way; a single click only
  selects); confirm one clip landed before adding the next. If a drop lands nowhere the
  target track is clipped below the viewport — raise the viewport height or close the
  media panel. A track header's bin deletes the whole track row (reload restores the
  default two-track layout).
- **Trim:** timeline zoom ~40 px/s; Cut + Delete for frozen/silent heads and tails;
  **Auto Align Clips** to close gaps.
- **Export:** High quality / FullHD / MP4 — 1920×1080 (16:9) or 1080×1920 (9:16).
  Exports live in **My Videos** (upstream notes a 40-day window) — download same day.
- **Always:** public gallery / sharing OFF, "Automatically enhance my video prompt" OFF,
  no music generated into clips.
