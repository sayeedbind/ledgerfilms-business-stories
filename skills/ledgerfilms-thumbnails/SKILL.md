---
name: ledgerfilms-thumbnails
description: Make scroll-stopping, eye-catching thumbnails for LedgerFilmsHQ videos (long-form 1280×720) and Shorts covers (1080×1920) in Artistly (app.artistly.ai, Advanced AI Image Designer), from the video's own frames or a generated concept image, under the channel's thumbnail rules — max 3 words, one frame or symbolic object, amber #FFB000 channel text, 10% zoom readability test, PNG + JPG under YouTube's 2 MB limit, two variants (A/B) filed with the upload pack. Use whenever a LedgerFilms video or Short needs a thumbnail or cover, when the upload pack's thumbnail brief has to become a real file, or when an existing thumbnail needs a rebuild. Verified live 2026-11-13 on SH-20261111-nvidia-alone.
---

# LedgerFilms Thumbnails — Artistly production skill

Why this skill exists: until 2026-11-13 the system had thumbnail **rules** (the brief
template, `docs/titles-thumbnails-metadata.md`, the finishing packaging triangle) but no
skill that **makes** one — thumbnails were improvised locally per film. The owner
designated **Artistly** (app.artistly.ai — same provider as VideoExpress; account plan
“Artistly Unlimited (Full Pay)”, login in the Secure Vault) as the thumbnail tool, and
this workflow was proven end to end on a real Short before being written down
(2026-11-13 test: 3 variants built, exported and verified; the clean one is filed as
`SH-20261111-nvidia-alone-THUMB-B-artistly.png`).

## The one rule

**The thumbnail is the film's single strongest frame or symbol, plus at most 3 words,
readable at 10% zoom.** If it needs a paragraph to work, it fails. The thumbnail and the
title divide the labour: the title names the story, the thumbnail carries the number or
the emotion — **never repeat the title's words on the thumbnail**.

## Before Artistly: the brief (blocking)

Fill `templates/thumbnail-brief.md` first — no editor work before it exists:

- **Text: max 3 words**, ideally the load-bearing figure + one impact word
  (“$190 BILLION / GONE”, “$2.5 TRILLION / ONE WEEK”). Numbers are checked against the
  research brief like any other claim — a thumbnail figure is a factual claim.
- **Frame:** one scene/moment from the video itself, same grade (teal-and-amber). A
  generated concept image is allowed as the B variant, never as a fake “scene” the film
  doesn't contain.
- **One face/emotion or one symbolic object**, huge at mobile size. No charts, no
  paragraphs, no fake logos, no model-rendered text (the words are set in the editor,
  never generated into the image).
- **Pairing:** write the title beside the thumbnail text and check they don't repeat.

## The route: Advanced editor, not the Thumbnail Agent

- **Production route = Create Design → Advanced AI Image Designer** (editor.artistly.ai),
  a Canva-style canvas editor. It is the only place an **exact** canvas size exists
  (custom Width × Height): **1280×720** long-form, **1080×1920** Shorts covers.
- **Do NOT use** AI Design Agents → “Youtube Thumbnails” (“Recreate Thumbnail” /
  “Videos to Thumbnail”) as the production route: it takes only a YouTube URL and a
  quantity (1–10) — no prompt, no style, no size, no text control. It cannot follow the
  brief or the channel grade. (It also cannot make a thumbnail for an unpublished video
  from a frame.)
- The Fast AI Image Designer's ratios are near-misses, not deliverables (its 16:9 is
  1344×768, not 1280×720). Generation **inside the editor** (AI Designer panel, 9:16 /
  16:9) is the approved way to make a concept variant — with the resize trap in the
  quirks list below.

## Workflow

1. **Pick the base frame from the RAW export** (before burned captions/overlays are
   added in finishing) or from a clean VE still — a frame with caption text burned in is
   not a base. Extract 2–3 candidates and pick by eye: one strong subject, dark or clean
   space where the text will sit.
2. **Create the project at the exact size.** Advanced editor → Create Project → custom
   Width × Height (long-form 1280×720; Short 1080×1920). **Quirk: the Width and Height
   fields overwrite each other — type Height first, then Width, and verify both numbers
   before clicking Create.** Name the project with the video's ID:
   `LF-YYYYMMDD-topic-THUMB` / `SH-YYYYMMDD-topic-THUMB`.
3. **Place the base.** Images panel → Upload Image → **Use Image**, scaled to fill the
   canvas edge to edge. (If the Upload button exposes no file picker to your browser
   tool, the Custom Character panel's file input works and lands the image the same
   way — verified 2026-11-13.)
4. **Optional treatments** (only where the frame earns them): AI Upscaler (“Only
   Upscale”), Object Remover, Inpainting, Instant Scene background replace. There is
   **no true background remover** in the editor — background *replace* is the tool.
5. **Set the text.** Text panel → **Add a heading per line** (the Duplicate button does
   not reliably duplicate a text box — build each line fresh). Channel treatment:
   **Bold**, line 1 (the figure) in **amber #FFB000** (the colour picker takes hex),
   line 2 (the impact word) in **white**; fonts verified present include Arial,
   Arial Black, Impact, Montserrat, Poppins, Roboto, Bangers — pick one heavy face and
   keep it across the channel's thumbnails.
   - **Width discipline (the 2026-11-13 defect):** keep every line **≤85% of canvas
     width with clear margins on both sides**. On the test, a line stretched edge to
     edge clipped its first/last letters on 2 of 3 variants (A and C) — a clipped
     letter is a failed thumbnail, not a style. Size from the rendered text; the
     font-size field can show stale values.
   - **Never drag a text box by its side handles** — it stretches the glyphs
     horizontally. Resize via the font-size field, re-centre via alignment.
   - **Placement:** Shorts — text in the **top third** (the feed UI covers the bottom
     and right rail). Long-form — keep clear of the **bottom-right** (duration badge).
   - **No outline/shadow control exists** in the editor. Legibility comes from frame
     choice (dark/clean space behind the words); if a frame is busy behind the text,
     put a dark rectangle from the Shapes panel behind the text block and lower its
     transparency instead of fighting the image.
6. **Save** (Save Changes — allow ~20–30 s; the editor is slow) and **Export → PNG**.
   Download the export **the same day**: Personal Designs are retained only **1 year**.
7. **File it like the long-form precedent:** in the video's goal `files/`, named
   `<video-id>-THUMB-A-artistly.png` (+ `-B` for the second variant), with a **JPG copy
   beside each PNG** (quality ~90). **The upload file must be ≤2 MB** (YouTube's
   thumbnail limit): a PNG over 2 MB (the test's variant A was 2.19 MB) is uploaded as
   its JPG, never re-exported smaller.
8. **Make two variants** when the film matters: **A = the film's own frame**,
   **B = the concept/generated variant** (or a second frame). The owner picks at
   upload, as with the AI Sell-Off long-form precedent.

## Concept variant (AI generation inside the editor)

- AI Designer panel → Image Generator → prompt in the channel style line
  (“Cinematic AI-illustrated documentary art, painterly digital illustration … dramatic
  low-key lighting, film grain, no text, no watermark”) → size 9:16 or 16:9 → place
  full-canvas.
- **Trap (verified): placing a generated image auto-resizes the canvas to the
  generation's own size** (a 1080×1920 project became 768×1344). After placing, open
  Settings (gear) and **Resize the canvas back to the exact deliverable size**, then
  re-check the text margins — the text moves with the resize.
- **Watermark: none** — verified on a generated export 2026-11-13 (full image + zoomed
  corner). Still check every generated export before filing; a watermark = regenerate,
  never ship.

## Verification gate (blocking — the export is checked, not assumed)

For each variant, on the **downloaded file**:

- [ ] Dimensions exact (1280×720 / 1080×1920) — read the file, not the project page
- [ ] Upload copy ≤2 MB (JPG if the PNG is over)
- [ ] **10% zoom test:** shrink to 10% (128×72 / 108×192) — every word still readable,
      the subject still identifiable
- [ ] No clipped or edge-touching letters; text inside its margins on all sides
- [ ] No watermark; no model-rendered text anywhere in the image
- [ ] Works with no text (the frame alone still says something) — brief checklist
- [ ] Title + thumbnail shown side by side: no repeated words, figure matches the brief
- [ ] Both variants + JPG copies in `files/`; the upload pack names the files

A failure returns to the editor step that caused it (resize trap → step “Concept
variant”; clipping → text width discipline), never to a local patch-up of the exported
PNG — the Artistly project is the source and stays editable.

## Verified quirks & timings (2026-11-13, Artistly 6.5)

- Create Project Width/Height fields overwrite each other → Height first, then Width,
  verify before Create; a stray wrong-size project can be deleted from Recent projects.
- Images-panel Upload may expose no file input to an automated browser → use the Custom
  Character panel's file input instead.
- Text-box Duplicate is unreliable → fresh heading per line.
- Font-size field can display stale values → judge size from the rendered text.
- Canvas zoom can jump after a font change → fit-to-screen control restores it.
- Editor steps (Create, Save) take ~20–30 s each; budget **~10–15 min per finished
  thumbnail** once the route is known (the 3-variant first test took ~40 min including
  a ~15 min upload-approval wait and first-time mapping).
- The account has no credits/meters and nothing in this workflow was paywalled
  (“Artistly Unlimited (Full Pay)”, checked across dashboard, agents, assistants and
  the editor).

## References

- `references/artistly-ui-map.md` — the mapped app: menus, editor panels, size tables,
  export flow, and the Thumbnail Agent's limits, all as observed live 2026-11-13.
- Channel rules this skill executes: `../../templates/thumbnail-brief.md`,
  `../../docs/titles-thumbnails-metadata.md`, filmcraft `references/finishing.md`
  (title–thumbnail–first-30s packaging triangle).
