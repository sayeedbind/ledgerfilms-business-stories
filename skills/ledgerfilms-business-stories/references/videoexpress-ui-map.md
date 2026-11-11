# VideoExpress UI map (as used by the merged workflows)

*Operational notes distilled from the three upstream playbooks. VideoExpress changes its
UI — if a label differs, follow the PLAYBOOK's intent and note the change in the repo.*

- **Create a scene:** create image first (with Consistent Character reference slots:
  Ref 1 = character master, Ref 2 = location/environment master where supported),
  then create video from that image.
- **Style routing (channel look):** Image Type **Photorealistic (Cinematic)**,
  Creative mode **off**. The LedgerFilms style line travels inside the prompt text.
- **Narration route (owner directive, 2026-11-04): per-clip voiceover in the
  generation dialog.** Each generation shows a **video prompt** and an **audio /
  voiceover prompt**: visual in the video prompt, that clip's exact narration line
  in the voiceover field, locked voice (Emotion Andrew Multilingual, speed 1,
  pitch 0) selected, then generate — the clip returns with its voiceover on it.
  Plan lines at ≤~20 words / ≤120 characters (the voiceover field is short; verify
  its current limit on the first clip of a run). **Never** use the standalone
  Import Media → Text to Speech panel for narration — that route is retired.
- **Single-voice rule (2026-11-07):** the **video prompt describes visuals only** —
  never paste the narration line, quoted speech or "narrator says" into it; the
  model voices any line it is given and the voiceover then says it a second time
  (doubled narration). **Video Only (No Sound) stays OFF** on narrated clips —
  ticking it kills *all* audio, including the voiceover.
- **The dialog trap:** before EVERY submission, check the settings *inside the generation
  dialog* — its ratio selector can reset to 9:16, prompt-enhancement can re-tick,
  and the **voiceover field / voice selection can reset** after a re-render,
  independently of the project bar. Fix only what reset; keep references; confirm
  the voiceover text is present before every Generate click.
- **Clip duration:** with a voiceover attached, the clip's length **follows the
  voiceover playtime automatically** — do not set a Manual Video Length that
  truncates the line. Manual length (up to 10 s, Advanced Mode ON, enhancement OFF)
  is for silent B-roll clips only. PLAYBOOK §6.
- **Parallel renders:** up to 5 concurrent video jobs on many accounts — the visible
  account limit is the rule. A full queue is a wait state, not an error.
- **Assembly:** Media Library → My Media → My AI Videos → **drag** each completed clip
  onto the timeline (a single click only selects); confirm one clip landed before
  adding the next. There are **no narration audio assets to drag** — each clip
  already carries its voiceover. If a drop lands nowhere the
  target track is clipped below the viewport — raise the viewport height or close the
  media panel. A track header's bin deletes the whole track row (reload restores the
  default two-track layout).
- **Trim:** timeline zoom ~40 px/s; Cut + Delete for frozen/silent heads and tails;
  **Auto Align Clips** to close gaps.
- **Export:** High quality / FullHD / MP4 — 1920×1080 (16:9) or 1080×1920 (9:16).
  **Exports are hard-capped at 600 s:** the dialog warns "your movie will be
  reduced" and the render cuts at exactly 600.00 s, silently dropping the end —
  trim longer projects to ≤600 s or export in parts and splice (PLAYBOOK §10).
  Exports live in **My Videos** (upstream notes a 40-day window) — download same day.
- **Always:** public gallery / sharing OFF, "Automatically enhance my video prompt" OFF,
  no music generated into clips.
