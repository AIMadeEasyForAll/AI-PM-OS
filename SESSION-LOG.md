# Session Log: Building AI-PM-OS

A record of how this repository was built and published, plus the exact steps used for the companion Substack walkthrough ("Stop Drowning in Product Documents"). Kept here so future sessions (and future you) don't have to re-derive any of this.

## What got built

A full `AI-PM-OS` repository, structured as:

```
AI-PM-OS/
├── README.md
├── LICENSE
├── CLAUDE.md
├── .github/copilot-instructions.md
├── skills/            (8 files: feature-scoping, discovery, prioritization,
│                        roadmap, metrics, experimentation,
│                        stakeholder-management, ai-evaluation)
├── artifacts/         (6 templates + diagrams/ with 4 .drawio files)
├── commands/          (6 reusable prompts)
├── mcp/                (5 integration docs: github, jira, notion, figma, slack)
├── settings/           (4 context files: glossary, personas, business-context,
│                        product-principles)
└── projects/
    ├── project-a/      (worked example: Saved Posts Redesign PRD)
    ├── project-b/      (empty, ready for the next project)
    └── project-c/      (empty, ready for the next project)
```

Every file has real, usable content — no placeholders — matching the structure described in the Substack draft.

## How it got published to GitHub

1. Created the repo locally, committed everything to `main`.
2. Created an **empty** repo at `https://github.com/AIMadeEasyForAll/AI-PM-OS` via the GitHub website (not via `gh repo create` — the fine-grained PAT didn't have repo-creation permission).
3. Pushed local `main` to `origin/main`.

### Snag hit, and how it was resolved

Pushing failed twice with `403 Permission denied`, for two different reasons:

- **First attempt** failed as `ManiShergill` — macOS Keychain had a cached GitHub credential for the wrong account.
- **Second attempt** (after authenticating `gh` with the `AIMadeEasyForAll` PAT and running `gh auth setup-git`) failed again, this time as `AIMadeEasyForAll` — the fine-grained PAT didn't have sufficient permission on the new repo.
- **Fix:** Added `ManiShergill` as a collaborator on `AIMadeEasyForAll/AI-PM-OS` and accepted the invite, then pushed using the cached `ManiShergill` keychain credential directly (bypassing the `gh`-configured helper for that one command):
  ```bash
  git -c credential.helper= -c credential.helper=osxkeychain push -u origin main
  ```

**Lesson for next time:** if a push fails with a permission error (not a credential prompt), it's almost always a stale cached credential for the wrong account, or a PAT scoped too narrowly (missing repos, or missing "Contents: Read and write" / "Administration" permissions). Check `git config --get-all credential.helper` and `gh auth status` first.

## Substack walkthrough: VS Code Commit & Push

For readers doing this entirely through the VS Code UI, no terminal required:

1. **Source Control** — click the branching-line icon in the sidebar. Changed files appear automatically.
2. **Review** — click any file to see a diff before committing.
3. **Stage** — click the `+` next to a file, or next to "Changes" to stage everything.
4. **Commit** — type a short message, then click the checkmark (or `Cmd+Enter`).
5. **Sync Changes** — click the button that replaces "Commit" once you've committed. This pushes your commit and pulls anything new from GitHub, in one click.

## Substack walkthrough: Test Your Connection (Git ↔ GitHub with a PAT)

1. Create a file: `test.md`
2. Add one line: `# My First GitHub Commit`
3. Stage → commit → **Sync Changes**.
4. If prompted for a username/password: username is your GitHub username, password is your **PAT** (not your real GitHub password).
5. Refresh your repo page on GitHub.

If `test.md` appears: connection confirmed. Delete `test.md` afterward — it was just a test.

**Troubleshooting note for readers:** if Sync Changes fails outright instead of prompting for a password, it usually means an old GitHub login is already cached on the machine. Clear it from Keychain Access (Mac) or Credential Manager (Windows) and retry.

## Still open

- **Screenshot: "Claude generating a PRD"** — needs a live, interactive Claude session run by the user (attach this repo, run the `create-prd` command against a real feature) — not something that can be produced after the fact.
- Token used during setup (PAT name: `Demo`) was pasted in plaintext during this session — recommended it be revoked/rotated.
