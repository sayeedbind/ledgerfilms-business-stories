# Push this repo to your GitHub

This folder is a complete, git-ready repository (structure modelled on
`ai-playbooks/realistic-mini-dramas`). To publish it under your own account:

```bash
cd ledgerfilms-business-stories
git init && git add . && git commit -m "LedgerFilms workflow v1.0"
gh repo create ledgerfilms-business-stories --private --source=. --push
```

No `gh` CLI? Create an empty repo on github.com first (no README), then:

```bash
git remote add origin https://github.com/<your-name>/ledgerfilms-business-stories.git
git branch -M main && git push -u origin main
```

**Private is the right default** — the topic bank and production calendar are your
competitive plans. If you make it public later, `SYSTEM-PROMPT.md` loads `PLAYBOOK.md`
by raw URL, so update that URL to your repo in both `SYSTEM-PROMPT.md` and `README.md`.

Updating later: edit files in place, `git add . && git commit -m "…" && git push`.
Every agent using the raw-URL prompt picks up the new PLAYBOOK automatically.
