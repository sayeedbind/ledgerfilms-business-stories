# Narration & sound — voiceover made with each clip

- **One narrator for the channel.** Record the exact voice name + settings in the bible
  template the first time, then reuse forever. Locked channel voice: **Emotion Andrew
  Multilingual, speed 1, pitch 0** (any change is an owner decision).
- **Route (owner directive, 2026-11-04): per-clip voiceover in the generation dialog.**
  In VideoExpress every generation shows a **video prompt** and an **audio / voiceover
  prompt** for that clip. Put the visual in the video prompt; put that clip's **exact
  narration line** in the voiceover field; select the locked voice + settings; generate.
  The clip comes back with its voiceover on it, its length follows the voiceover, and
  sync is structural. Do this for **every** clip.
- **Never separate.** No standalone Import Media → Text to Speech chunks, no My AI Audio
  narration assets, no separate narration track at assembly. That route was retired on
  2026-11-04 by the owner; it is not a fallback. If the voiceover option is missing or
  fails, stop and report — do not improvise separate narration.
- **Fit the field.** Plan each line at ≤~20 words / ≤120 characters; verify the dialog's
  current voiceover-field limit on the run's first clip and never exceed the smaller of
  (that limit, ~25 words / 10 s spoken). Split a longer line across two beats/shots.
  Never truncate a line, and never paste narration text into the video prompt.
- **The single-voice rule (owner correction, 2026-11-07).** The video prompt is
  **visuals only** — no narration line, no quoted speech, no "narrator says" —
  because the video model voices any line it is given, and the clip's voiceover
  then repeats it: doubled narration (a Short's v1 shipped exactly this defect).
  The visuals-only prompt is the kill switch. **"Video Only (No Sound)" stays
  OFF** — ticking it killed ALL audio including the voiceover on the repair run.
- **Locked means per-clip locked.** An accepted clip's voiceover is never re-recorded,
  cut, speed-changed or swapped. A mispronunciation is fixed by regenerating **that
  clip** with the respelled word in its voiceover text (screenplay pronunciation list).
- **Verify every clip's voice** at the segment checkpoint: present, locked voice, full
  line, matching its AUDIO cell — and **listen to the tail** of each clip for a
  doubled final word (doubling passes a words-in-order check; only the tail
  listen catches it). Silent / truncated / wrong-voice = failed clip,
  regenerate (max 3 attempts, one variable per retry).
- **Voices and permission:** system voices by default. A cloned voice only with the
  speaker's documented permission for this use.
- **Mix:** clips are generated WITH the production sound described in their prompts —
  transient, action-tied ambience and effects, no dialogue, never silent video —
  mixed low under that clip's voiceover. Music enters only at assembly: one track,
  low, ducked; never generated inside clips (per-clip music makes cuts unmatchable).
- **Pacing maths:** documentary narration ≈140–150 wpm. Long-form script 1,350–1,500
  words ≈ 10 min. Short 115–150 words ≈ 45–60 s. Runtime is the sum of the clips'
  measured durations; if a take runs long, the script was long — fix the *next*
  script, not this audio.
