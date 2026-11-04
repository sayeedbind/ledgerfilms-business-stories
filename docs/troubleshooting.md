# Troubleshooting

| Symptom | Likely cause | Fix |
|---|---|---|
| ChatGPT browser automation won't start ("process launcher failed") | Full access not on *for this chat* | `CHATGPT_SETUP.md` — Settings AND the per-chat permissions menu, both |
| Dialog exports 9:16 when the project is 16:9 | Generation dialog ratio reset independently | Re-check ratio **inside the dialog** before every submission (PLAYBOOK §7.3) |
| Scenes turn into stickmen / cartoon | Creative mode or wrong image type crept in | Image Type = Photorealistic (Cinematic), Creative mode OFF, style line at the start of the prompt |
| Founder's face changes between clips | A scene image replaced the master, or bible paraphrased | Regenerate from the master; paste bible blocks verbatim; Consistent Character on every clip |
| Garbled numbers / signage in scenes | Model asked to render text | Numbers rule (PLAYBOOK §5): abstract shapes in scenes, real numbers as edit overlays |
| Runtime ≠ plan | Clip durations follow their voiceovers — the summed clip total is the runtime | Add/remove whole beats (picture + voiceover together); never speed/chop a clip's voiceover |
| Queue "stuck" | All parallel slots busy (often 5) | Wait for a slot; never duplicate the job |
| A clip keeps failing (3 attempts) | One stubborn variable | Change ONE variable per retry; if still failing, restage the beat simpler (one subject, locked camera) and escalate to the user |
| Era errors (smartphone in 1998) | Era block missing from that prompt | Era & outfit block is mandatory in every prompt; era errors are QC fails |
| Script claim challenged / wrong | Weak sourcing | Same-day pinned correction + description fix; log in the research brief |

| Voiceover text does not fit the dialog's voiceover field | The clip's line is too long for the per-clip voiceover option | Split the line into two beats = two clips/shots (plan ≤~20 words / ≤120 characters per clip, PLAYBOOK §6/§8); never truncate the line and never move it to a separate TTS tool |
| Clip generated with no voiceover / silent clip | Voiceover field was empty, or the voiceover option/voice selection reset in the dialog before Generate | Regenerate that clip with the voiceover text entered and the locked voice selected; check the field immediately before every Generate click (dialog settings reset independently) |
| Clip's voiceover is truncated or in the wrong voice | Line exceeded the field limit, or the dialog's voice selection reset | Shorten/split the line, re-select the locked channel voice (Emotion Andrew Multilingual, speed 1, pitch 0), regenerate that clip only |
| Name/number mispronounced in a clip | TTS read the spelling literally | Respell the word inside **that clip's voiceover text** (pronunciation list) and regenerate that clip; never patch with separate audio |
| Voiceover runs over black / after the picture in an export | A separate narration track was built (retired route) | Rebuild per PLAYBOOK §8: voiceover generated **with each clip** — there is no separate track to displace; do not export the displaced cut |
| Drag from library lands nowhere | Target track clipped below the viewport (media panel open, short viewport) | Raise the browser viewport height or close the media panel; drop again |
| Second timeline track disappeared | A track header's bin deletes the whole track, not just clips | Reload the page — the default two-track layout returns |
| Delete key no-op on a timeline clip | Editor quirk | Select the clip and use toolbar delete/cut; verify before re-adding |
