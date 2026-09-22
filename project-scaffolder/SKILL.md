---
name: project-scaffolder
description: Scaffold a production-ready project from requirements by clarifying requirements, selecting an appropriate stack, creating project conventions, and verifying the generated application.
---

# Project scaffolder

## Purpose

Turn an idea or PRD into a coherent, minimal, production-ready project foundation without inventing unnecessary architecture.

## When to use

Use when starting a new application, repository, service, monorepo, or major project foundation.

## When not to use

Do not use for ordinary feature work in an existing project.

## Procedure

1. Inspect the supplied requirements or PRD.
2. Identify genuinely ambiguous requirements and ask focused questions.
3. Determine functional and non-functional requirements.
4. Select the smallest suitable architecture and stack.
5. Explain consequential technology choices before implementation when they are not predetermined.
6. Scaffold the project.
7. Generate project operating documents:
   - `AGENTS.md`
   - `DESIGN.md`
   - `WORKFLOW.md`
   - `README.md`
8. Install dependencies.
9. Run the narrowest relevant checks.
10. Fix scaffolding errors.
11. Report the generated structure, decisions, and verification.

## Decision rules

- Never add technology because a template happens to contain it.
- Every dependency must have a reason.
- Prefer established project defaults when the user has already chosen a stack.
- Do not force authentication, databases, dashboards, or paid services unless requirements justify them.
- Keep generated architecture as simple as the requirements allow.
- Do not overwrite existing files without explicit intent.

## Verification

At minimum:
- dependency installation succeeds
- source builds or compiles
- configured lint/type checks pass
- configured tests pass
- generated documentation matches the selected architecture

## References

Load only the references needed for the current project.
