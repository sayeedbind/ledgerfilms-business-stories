# Troubleshooting

| Symptom | Likely cause | Fix |
|---|---|---|
| ChatGPT browser automation won't start ("process launcher failed") | Full access not on *for this chat* | `CHATGPT_SETUP.md` — Settings AND the per-chat permissions menu, both |
| Dialog exports 9:16 when the project is 16:9 | Generation dialog ratio reset independently | Re-check ratio **inside the dialog** before every submission (PLAYBOOK §7.3) |
| Scenes turn into stickmen / cartoon | Creative mode or wrong image type crept in | Image Type = Photorealistic (Cinematic), Creative mode OFF, style line at the start of the prompt |
| Founder's face changes between clips | A scene image replaced the master, or bible paraphrased | Regenerate from the master; paste bible blocks verbatim; Consistent Character on every clip |
| Garbled numbers / signage in scenes | Model asked to render text | Numbers rule (PLAYBOOK §5): abstract shapes in scenes, real numbers as edit overlays |
| Narration length ≠ plan | Narration is locked and sets runtime — this is expected | Cut picture to the voice (§9.4); never speed/chop audio |
| Queue "stuck" | All parallel slots busy (often 5) | Wait for a slot; never duplicate the job |
| A clip keeps failing (3 attempts) | One stubborn variable | Change ONE variable per retry; if still failing, restage the beat simpler (one subject, locked camera) and escalate to the user |
| Era errors (smartphone in 1998) | Era block missing from that prompt | Era & outfit block is mandatory in every prompt; era errors are QC fails |
| Script claim challenged / wrong | Weak sourcing | Same-day pinned correction + description fix; log in the research brief |

| Narration text box caps at 120 characters | You are in the generation dialog's "Narration Video" flow | Use the standalone Import Media → Text to Speech route (PLAYBOOK §8); the dialog flow cannot build a long voice-over |
| Long TTS import produces no audio and no error | Import above the practical ~1,100-character cap (counter says 2,400) | Split narration into ≤1,000-character sentence-boundary chunks; verify each import created a My AI Audio asset |
| Narration chunk replaced instead of appended | Each Import Speech replaces the panel's pending audio | The library keeps every import (My AI Audio, label = opening words); drag assets to the timeline in script order |
| Narration assets unfindable / wrong order | TTS panel shows only the latest import; My AI Audio mixes all past projects | Match chunks by their opening-words labels and recorded /library/download/<id> asset IDs, never by grid position |
| Drag from library lands nowhere | Target track clipped below the viewport (media panel open, short viewport) | Raise the browser viewport height or close the media panel; drop again |
| Second timeline track disappeared | A track header's bin deletes the whole track, not just clips | Reload the page — the default two-track layout returns |
| Delete key no-op on a timeline clip | Editor quirk | Select the clip and use toolbar delete/cut; verify before re-adding |
