# Audit report

This template structures the output of project-standards-audit. Fill in each section with findings from the inspection.

## Overview

- Project root: `<path>`
- Inspection date: YYYY-MM-DD
- Canonical startup documents check: passed | failed
- Project structure check: passed | failed
- Verification: passed | failed

## Canonical startup documents

| Document | Status | Notes |
|---|---|---|
| `AGENTS.md` | / | / |
| `DESIGN.md` | / | / |
| `WORKFLOW.md` | / | / |
| `README.md` | / | / |

### Lowercase duplicates

If lowercase variants were found (e.g., `agents.md`, `readme.md`), document:
- Source file: `<path>/<lowercase-name>`
- Content migrated: yes / no
- Target canonical document: `<path>/<uppercase-name>`
- Duplicate removed/renamed: yes / no

## Project structure

Observations about the project structure relative to project-scaffolder standards. Distinguish observed facts from recommendations.

## Verification

- Lint: result
- Typecheck: result
- Tests: result
- Build: result
- Overall status: passed / failed

## Recommended actions

1. ...
2. ...

## Documentation drift

Notes on any inconsistencies between documented claims and actual project behavior.