# ChatGPT setup

Adapted from the realistic-mini-dramas playbook (same requirement, unchanged mechanics).

On Mac/Windows, ChatGPT needs **Full access** before its browser automation can run —
without it you'll see errors like "process launcher failed" or "browser-control session exited".

1. **Settings → General → Permissions** → turn on **Full access**.
2. Back in the chat, open the **permissions menu in the message box** and choose Full access
   *for this chat* (turning it on in Settings only adds it to the menu).
3. **Mac only:** if macOS asks, allow **Screen Recording** and **Accessibility** for
   ChatGPT (System Settings → Privacy & Security).

If Full access doesn't appear, your plan/organisation may not offer it. Use Claude in
Chrome or the Claude desktop app instead — the same `SYSTEM-PROMPT.md` works there.

## Optional: a standing LedgerFilms Project / Custom GPT

Paste `PROMPT_COMPACT.md` (below its line) into the instructions field and enable
browsing/agent capability. Every new chat then opens with the Mode / Topic / Angle /
Sources intake, already knowing the channel's formats, bible and fact rules.
