# Integration: GitHub

## What it does

Hosts this entire operating system. GitHub is where skills, artifacts, commands, and settings live as version-controlled markdown, and where Claude or Copilot read them from when attached to the repo.

## Access

- Repository: [add your repo URL here]
- Required access: write access to push artifacts back; read access is enough to use the system.

## Common workflows

- **Attach the repo to Claude** to give it access to `skills/`, `artifacts/`, `commands/`, and `settings/` for the current conversation.
- **Open a PR for any change to a skill or template** — even solo, this gives you a diff and a history of why something changed, which a Google Doc revision history doesn't give you cleanly.
- **Save approved artifacts into `projects/your-project/`** as the final step of any workflow, so the next project (or the next person) can find it.

## Important commands

```bash
git clone [repo-url]
git checkout -b update-skill/feature-scoping
# edit the file
git add skills/feature-scoping.md
git commit -m "Tighten feature-scoping success-metric step"
git push origin update-skill/feature-scoping
gh pr create
```

## Notes for future you

If a skill or template stops matching how you actually work, edit it here — don't just work around it in the chat. The system only stays useful if the repo reflects current practice.
