---
name: project-standards-audit
description: Inspect existing projects for canonical startup documents, verify project structure against project-scaffolder standards, create missing documents, and return an audit report.
---
# Project standards audit

## Purpose

Inspect existing projects for missing or non-canonical startup documents, verify project structure against project-scaffolder standards, create missing canonical documents, and return a detailed audit report. Targets projects that have already been scaffolded or are otherwise established.

## When to use

Use when onboarding an existing project, verifying project documentation standards, or auditing a project before further development. Run as part of a project maintenance workflow.

## When not to use

Do not use for ordinary feature work in a project where documentation is already verified and up to date.

## Procedure

1. **Inspect the project root** — Examine the repository structure and identify all files matching the canonical startup-document filenames.
2. **Check for canonical startup documents** — Verify the presence of `AGENTS.md`, `DESIGN.md`, `WORKFLOW.md`, and `README.md` at the project root. These must use uppercase filenames.
3. **Inspect existing documents** — If startup documents already exist, read and evaluate them. Do not blindly overwrite. Preserve useful information and migrate content from lowercase variants (e.g., `agents.md`, `readme.md`) into the canonical uppercase document where appropriate.
4. **Create missing documents** — If any canonical startup document is absent, generate it using the project-scaffolder templates or appropriate project-specific content. Use uppercase filenames only.
5. **Check project structure** — Inspect the project structure against project-scaffolder standards. Avoid unnecessary restructuring of working application code. Only flag structural deviations that impact documentation consistency or standards compliance.
6. **Normalize filenames** — If lowercase variants of canonical documents exist (e.g., `agents.md`, `design.md`, `workflow.md`, `readme.md`), inspect them. Preserve useful information and migrate it into the canonical uppercase document. Safely remove or rename duplicates only when justified and after content migration.
7. **Verify the resulting project** — Run the project's existing checks (lint, typecheck, tests, build) to confirm the project is in a valid state after any changes.
8. **Return an audit report** — Produce a concise human-readable audit report summarizing findings, actions taken, and remaining issues.

## Decision rules

- Canonical startup-document filenames must always be uppercase: `AGENTS.md`, `DESIGN.md`, `WORKFLOW.md`, `README.md`. Never generate lowercase variants.
- Existing startup documents are inspected and preserved; only migrated or corrected when inconsistencies or non-canonical filenames are detected.
- Lowercase duplicates (e.g., `agents.md`) are migrated into the canonical document where useful content exists; they are then removed or renamed.
- Project structure is checked for consistency with project-scaffolder-generated foundations. Working application code is not restructured unless documentation standards cannot be met otherwise.
- Verification uses the target project's real tooling (lint, typecheck, tests, build). Generic commands are not substituted.
- The audit report distinguishes observed facts, potential issues, recommendations, and verification performed.

## Output

An audit report detailing:
- Which canonical startup documents exist and their status
- Any lowercase duplicates found and how they were handled
- Project structure observations relative to project-scaffolder standards
- Verification results
- Recommended actions

## References

- `references/startup-documents.md` — Canonical startup document definitions
- `references/project-structure.md` — Project structure checking guidelines
- `references/documentation-audit.md` — Documentation audit procedures
- `references/verification.md` — Verification procedures
- `templates/audit-report.md` — Audit report template