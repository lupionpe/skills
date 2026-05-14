# Issue tracker: Local Markdown

Issues and PRDs for this repo live as markdown files in `docs/issues/`.

## Conventions

- PRDs and issues share one flat directory: `docs/issues/`
- The PRD is `docs/issues/<YYYYMMDD>-prd-<feature-slug>.md`, using the user's local date when the PRD is created
- Implementation issues are `docs/issues/<NN>-<feature-slug>-<issue-slug>.md`, numbered from `01` per feature
- Triage state is recorded as a `Status:` line near the top of each issue file (see `triage-labels.md` for the role strings)
- Comments and conversation history append to the bottom of the file under a `## Comments` heading

## When a skill says "publish to the issue tracker"

Create a new file under `docs/issues/` (creating the directory if needed).

## When a skill says "fetch the relevant ticket"

Read the file at the referenced path. The user will normally pass the path or the issue number directly.
