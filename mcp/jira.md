# Integration: Jira

## What it does

Tracks engineering work — tickets, sprints, epics. This repo is the source of truth for *why* something is being built (PRDs, decisions); Jira is the source of truth for *whether it's been built yet*.

## Access

- Instance: [add your Jira URL here]
- Project key(s): [add project key, e.g. PROD]
- Required access: at minimum, read access to the relevant project; write access to create tickets from scoped work.

## Common workflows

- **After a PRD is approved** (via `commands/create-prd.md`), break it into stories with `commands/create-user-story.md`, then create the corresponding Jira tickets — link the ticket back to the PRD/artifact file in this repo so context isn't lost.
- **Pull ticket status into a roadmap or exec summary** when generating `commands/generate-roadmap.md` or `commands/write-exec-summary.md` — paste current sprint/epic status as input context.
- **Close the loop after launch**: update the linked decision log entry (`artifacts/decision-log-template.md`) once a Jira epic ships, rather than letting status live only in Jira.

## Important links

- Active sprint board: [add link]
- Backlog: [add link]

## Notes for future you

Jira tickets should reference the artifact file that scoped them (e.g. "see projects/project-a/prd.md"), not duplicate the scoping content into the ticket description — keep one source of truth.
