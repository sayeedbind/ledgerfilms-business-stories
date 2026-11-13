# Artistly UI map — as observed live 2026-11-13 (Artistly 6.5)

Account: plan **“Artistly Unlimited (Full Pay)”** (“Pay once, own it forever”), no credit
balance or usage meter anywhere checked, no locks/upgrade prompts found across the
dashboard, AI Design Agents, AI Design Assistants, Fast designer or the editor. Login is
email/password only (no SSO); the login is held in the Secure Vault. Re-check labels each
run — the app updates often (dashboard banner: “Welcome To Artistly v6.5”).

## Top level (app.artistly.ai)

- Nav: **Dashboard · Create Design · My Purchases**.
- Dashboard sections: “Artistly Image Designers” (AI Design Agents; AI Design Assistants;
  AI Image Designer v6; Advanced AI Image Designer; Kids Puzzles; AI Art Illustrator;
  AI Storybook Studio; Consistent Characters; AI Bulk Actions; My Flipbooks; Personal
  Designs; Community Designs) and “Artistly Other Tools & Resources” (Videos To GIF;
  Videos To Images; Bonus Tools; Niche Finder; Get Free Credits; Get VideoExpressAI…).
- **Create Design** → “Choose Your Designer”: **Fast AI Image Designer** (prompt-based,
  v6) or **Advanced AI Image Designer** (canvas editor, editor.artistly.ai). Thumbnails
  are made in the Advanced editor (see the SKILL).

## The Thumbnail Agent (not the production route)

AI Design Agents → category **“Youtube Thumbnails”** → two modes: **“Recreate
Thumbnail”** and **“Videos to Thumbnail”**. Both ask for exactly one input: a **YouTube
Video URL**; then a Thumbnail Preview, “Select Quantity” (1–10), “Select Folder” and a
**Generate Thumbnails** button. No prompt, upload, style, size or text control. Outputs
land in **Personal Designs** (Download Image / Edit this image; bulk download/move/
delete). Retention notice shown there: **personal designs are saved for 1 year** —
download finished work the same day.

## Fast AI Image Designer v6 (sizes — near-misses only)

1:1 1024×1024 · **16:9 1344×768** · 21:9 1536×640 · 3:2 1216×832 · 2:3 832×1216 ·
4:5 896×1088 · 5:4 1088×896 · 3:4 896×1152 · 4:3 1152×896 · 9:16 768×1344 · 9:21
640×1536. No exact 1280×720 or 1080×1920 — do not deliver from here.

## Advanced AI Image Designer (editor.artistly.ai) — the production route

- **Create Project** presets: Square 1080×1080, Landscape 1920×1080, Portrait
  1080×1350, Twitter Post 912×512, Small Thumbnail 100×100, Small Banner 300×300, plus
  **custom Width × Height** (any size accepted; 1280×720 and 1080×1920 verified).
  **Bug:** typing one dimension can overwrite the other — set Height, then Width, verify.
- **Left-rail panels:** Built-in Templates (Social Media and **Thumbnail** tabs,
  searchable, paged); Images (Upload Image, Choose from Design, default library with
  Use Image / Move / Remove); Text (textbox, heading, subheading, paragraph); AI Product
  Influencer; AI Designer (Image Generator — prompt + size buttons 1:1, 3:4, 16:9, 9:16;
  Mirror Magic — derive a prompt from a canvas image); Shapes (circle, rounded square,
  square, triangles, diamond); Settings (canvas Width/Height + Resize, background colour
  incl. transparent).
- **Text toolbar** (text selected): colour swatch **with hex entry**, font dropdown
  (Arial, Arial Black, Impact, Montserrat, Poppins, Roboto, Playfair Display, Lobster,
  Bangers…), Bold / Italic / Underline / Strikethrough, alignment, numeric font size.
  **No outline, shadow or text-background control found** (an unlabeled toolbar icon
  next to Bold did nothing observable). Duplicate does not reliably duplicate a text
  box; side-handle drags stretch glyphs; the size field can show stale values.
- **Layers:** “Layers” toolbar button → panel listing Workspace + each element with
  show/hide, lock, move up/down; top toolbar also has bring-forward/send-backward,
  transparency, duplicate, delete.
- **Image tools on the toolbar:** AI Upscaler (“Only Upscale” / “Improve Human Photos”),
  Instant Scene — Background Replace (Automatic / Manual-with-prompt; **no plain
  background-to-transparent remover**), Object Remover, Inpainting, AI Stylizer, Custom
  Consistent Character, Crop, Flip V/H, eyedropper, expand (outpainting).
- **Top bar:** Save Changes, Save As Template, Share, New Project, **Export** →
  **PNG** (“Best for sharing on the web”) / **JPG** (“Best for printing”). Export
  downloads to the browser's default folder (no destination picker).
- **Canvas auto-resize trap:** placing an AI-generated image can reset the canvas to
  the generation's size (1080×1920 → 768×1344 observed, with a “Canvas automatic
  dimensions initialized” notice). Fix via Settings → Resize back to the target size.
- Editor latency: Create/Save steps commonly take ~20–30 s.
