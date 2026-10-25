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
