# Multishot prompt format (LedgerFilms adaptation)

*Method adapted in original wording from the upstream VideoExpress Scripting skill's
approach (prompt pack + bible + tagged multishot prompts). That skill is CC BY-NC 4.0 —
see `../../../LICENSE-NOTICES.md`. This file is our own summary for LedgerFilms use.*

## The pack
A video is planned as a **prompt pack**: bible first, then per-clip entries —
a start-image prompt, then a video prompt. Only text inside the prompt blocks is pasted
into VideoExpress; headings and notes are production metadata and must never leak into a
generation prompt (no clip IDs, filenames, URLs or asset codes inside the pasted text —
the ID prefix below is the single exception, used to match takes to the pack).

## Video prompt skeleton
```
[Clip 07]
[REFERENCE USE] Use the supplied image as the opening frame. Reference 1 is the founder
master (identity). Reference 2 is the location master (layout).
[IDENTITY / CONTINUITY] <founder block, verbatim> <era & outfit block, verbatim>
[SCENE] <location block, verbatim> + this beat's specific props, counted and placed.
[ACTION] Total duration 8s. SHOT 1 (0–3s, wide): … SHOT 2 (3–6s, medium, hard cut): …
SHOT 3 (6–8s, close, hard cut): … One clear action per shot, cause before effect.
[CAMERA] Locked / slow push-in to <destination>. Never moves without a destination.
[LIGHT AND IMAGE] <style line, verbatim> + this scene's light source and time of day.
[PRODUCTION SOUND] Transient sounds tied to the visible actions only. No music.
[NEGATIVES] No text, no watermark, no logos, no music, no speech, no extra people,
no modern objects, no distorted hands.
```

## Rules
- **Nouns, not intentions.** The engine renders what you name — count people and props,
  place them left/right, name the exact objects. Delete decorative nouns.
- **Positives except in [NEGATIVES].** Everywhere else, state what IS there and what
  stays still. Only [NEGATIVES] may exclude, each item starting "No".
- **Quotation marks = speech.** Quote nothing — narration is layered separately, and a
  stray quote will make a character "speak" it.
- **Bible blocks verbatim**, including in start-image prompts (which start `[Image 07A]`).
  When an accepted start image improves on the bible's wording, update the bible to the
  image's wording once, then stay verbatim with the new version.
- **Match the frame, not the plan.** Before writing a chained prompt, look at the actual
  opening frame and describe its real geometry.
- **Camera:** one move per clip at most, named the same way everywhere, always with a
  destination; never pan back into space that left the frame.
- **Prompt box ≈6,000 characters.** Trim repeated style/negative text first, never bible
  identity text.
- **Detail holds only at the size it was last drawn.** A push-in to a closer framing than
  the start image will redraw faces/props from text. Closer = new clip, new start image.
- **Multi-shot inside one generation:** distinct angles, explicit hard cuts, connected
  actions across cuts, same people/wardrobe/stage in every shot. Don't also ask for
  "one continuous shot" — the two instructions fight.
