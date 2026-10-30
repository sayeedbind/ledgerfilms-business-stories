# Narration & sound

- **One narrator for the channel.** Record the exact voice name + settings in the bible
  template the first time, then reuse forever. Default narrator: a calm American-English
  system voice (the documentary upstream used a "Daniel Reed"-style presenter voice and
  an "Ethan Sterling"-style narration voice — pick ONE for LedgerFilms and lock it).
- **Route (field-tested 2026-10-30):** Import Media → Text to Speech (standalone panel).
  NOT the dialog's Narration Video flow — it caps its text box at 120 characters and each
  import replaces the pending audio, so it cannot build a long voice-over. The standalone
  tool accepts 2,400 characters but imports above ~1,100 can fail silently: use
  ≤1,000-character sentence-boundary chunks. Every import lands in My AI Audio labelled
  by its opening words (record asset IDs in script order). Generate once and lock.
- **Locked means locked.** Generate the narration once. Its real duration sets the video's
  runtime. No re-generation, cuts, silence-trimming or speed changes to hit a target
  length — adjust the picture instead (PLAYBOOK §9).
- **Voices and permission:** system voices by default. A cloned voice only with the
  speaker's documented permission for this use.
- **Mix (upstream reference method):** clips are generated WITH the production sound
  described in their prompts — transient, action-tied ambience and effects, no
  dialogue, never silent video. Narration sits on top, always intelligible; clip
  production sound stays in the mix, ducked low beneath the voice. Music enters only
  at assembly: one track, low, ducked; never generated inside clips (per-clip music
  makes cuts unmatchable).
- **Production sound inside clips:** transient, action-tied sounds only (a till drawer,
  a shutter, rain on a window). Never request "silence" (renders as rumble) and never
  background music in a [PRODUCTION SOUND] block.
- **Pacing maths:** documentary narration ≈140–150 wpm. Long-form script 1,350–1,500
  words ≈ 10 min. Short 115–150 words ≈ 45–60 s. If a take runs long, the script was
  long — fix the *next* script, not this audio.
