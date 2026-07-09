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

## Wayfinding operations

Used by `/wayfinder`. The **map** is a file with one **child** file per ticket.

- **Map**: `docs/issues/<effort>-map.md` — the Notes / Decisions-so-far / Fog body.
- **Child ticket**: `docs/issues/<effort>-NN-<slug>.md`, numbered from `01`, with the question in the body. A `Type:` line records the ticket type (`research`/`prototype`/`grilling`/`task`); a `Status:` line records `claimed`/`resolved`.
- **Blocking**: a `Blocked by: NN, NN` line near the top. A ticket is unblocked when every file it lists is `resolved`.
- **Frontier**: scan `docs/issues/<effort>-NN-*.md` for files that are open, unblocked, and unclaimed; first by number wins.
- **Claim**: set `Status: claimed` and save before any work.
- **Resolve**: append the answer under an `## Answer` heading, set `Status: resolved`, then append a context pointer (gist + link) to the map's Decisions-so-far in the map file.
