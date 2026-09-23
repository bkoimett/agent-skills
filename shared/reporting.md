# Reporting

Reports should contain:
- scope
- files changed or inspected
- decisions
- checks run
- failures
- remaining risks

Be concise and factual.

## Cross-skill lifecycle contract

The three documentation lifecycle skills follow this contract:

project-scaffolder creates (at project root, uppercase filenames):
- `AGENTS.md` — coding agent conventions
- `DESIGN.md` — architecture and UI/design decisions
- `WORKFLOW.md` — development, testing, Git, and release workflow
- `README.md` — human-facing setup and project overview

project-standards-audit ensures those documents exist, remain accurate, and follow project standards:
- Inspects for canonical startup documents
- Checks for and normalizes lowercase filename duplicates
- Verifies project structure consistency
- Creates missing canonical documents
- Returns an audit report

app-review creates/updates (at project root):
- `REVIEW.md` — persistent review artifact with findings, recommendations, and verification status
- Returns a concise human-readable review summary to the agent/user
- Does not modify application source code, configuration, dependencies, or runtime behavior
