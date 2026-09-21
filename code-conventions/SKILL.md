---
name: code-conventions
description: "NOT YET BUILT. Planned: enforce the same linting config, commit style, and README structure across every project, catching drift when a project's config quietly diverges from the builder's standard."
metadata:
  status: planned
---

# Code Conventions (planned)

## Problem this is meant to solve

`AGENTS.md` (from `project-scaffolder`) states conventions per project,
but nothing currently checks that a project's actual lint config, commit
history, and README structure still match those stated conventions over
time. This skill is the enforcement/audit layer, not the "state the rule"
layer — that already exists.

## Scope (draft — refine before building)

- A standard lint/format config per stack (ESLint/Prettier config for
  Node/TS, `gofmt`/`golangci-lint` config for Go) that gets dropped into
  every new project identically, instead of each project's config
  drifting from hand-tweaking.
- A commit-message linter/check matching the Conventional Commits +
  issue-number format already defined in `WORKFLOW.md`'s template — this
  skill would be what actually verifies commits follow it, not just
  documents that they should.
- A README structure check against `README.template.md` — flags when a
  project's README has drifted from the standard shape (missing the
  "Project docs" cross-reference section, for example).

## Before building

- This one depends most heavily on `project-scaffolder` already being in
  use on a few real projects — build it after there's drift to actually
  observe and correct, not before.
- Decide whether this runs as a CI check (feeding into
  `cicd-consistency`) or as something the agent runs proactively before
  a commit.

## Structure (matches project-scaffolder's pattern)

```
code-conventions/
├── SKILL.md
├── templates/       — the standard lint/format configs per stack
└── references/      — what "drift" looks like and how to fix each kind
```
