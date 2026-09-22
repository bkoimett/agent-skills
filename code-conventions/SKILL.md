---
name: code-conventions
description: Audit and maintain project coding conventions, tooling conventions, file organization, and documented standards without inventing new conventions.
---

# Code conventions

## Purpose

Detect convention drift and help keep implementation consistent with the project's established rules.

## Procedure

1. Inspect `AGENTS.md`, `DESIGN.md`, and `WORKFLOW.md` when present.
2. Identify the project's stack and tooling.
3. Inspect representative source files and configuration.
4. Run available lint, typecheck, test, and formatting checks.
5. Compare implementation against documented conventions.
6. Report concrete drift with file references.
7. Apply fixes only when requested or clearly part of the task.

## Decision rules

- Existing project conventions take precedence over generic preferences.
- Do not create conventions solely to justify a refactor.
- Prefer minimal changes.
- Separate factual violations from recommendations.

## Verification

Run the relevant project checks after any fixes.
