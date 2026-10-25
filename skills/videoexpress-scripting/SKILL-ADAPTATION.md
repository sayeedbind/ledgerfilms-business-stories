# SKILL-ADAPTATION — what we took as method, restated

Our own notes on the upstream scripting method, written for LedgerFilms. (Method summary,
not the upstream text — see README.md in this folder for the licence position.)

1. **Prompt pack, not prompts.** Plan the whole piece as one living document: overview →
   global rules → bible → per-scene start images and clip prompts → edit/QC notes.
   Clip/image IDs (`[Clip 07]`, `[Image 07A]`) stay stable once generation starts.
2. **Core Bible.** Character, outfit and location descriptions written once and pasted
   verbatim into every prompt. When a generated frame improves on the bible, update the
   bible to match the frame — centrally, once.
3. **Two engine facts.** (a) The model renders nouns, not intentions — audit every noun.
   (b) Each generation knows only its opening frame + its prompt — anything not visible
   or stated will be invented.
4. **Multishot sections.** [REFERENCE USE] [IDENTITY/CONTINUITY] [SCENE] [ACTION]
   [CAMERA] [LIGHT AND IMAGE] [PRODUCTION SOUND] [NEGATIVES] — see our template in
   `../ledgerfilms-business-stories/references/multishot-prompt-format.md`.
5. **Style discipline.** A stylised look needs its style anchor at the very start of the
   video prompt and repeated in [LIGHT AND IMAGE], plus anti-drift negatives. For
   LedgerFilms the anchor is the channel style line (cinematic photoreal).
6. **Failure-fix method.** Diagnose by mechanism (what made the engine do that?), fix the
   prompt rule globally, and sweep every not-yet-generated clip with the same risk.
   A failure that survives two rewordings gets a one-variable-at-a-time test series,
   not a third rewording.
7. **Generation checkpoints.** In automated runs, the human approves start images and
   keeps/ditches takes; the agent pastes prompts exactly as written and never skips a
   checkpoint the pack defines. (LedgerFilms default: user approval only at master-image
   stage and at final QC — see PLAYBOOK.)
