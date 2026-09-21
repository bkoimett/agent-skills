---
name: cicd-consistency
description: "NOT YET BUILT. Planned: generate the same GitHub Actions workflow pattern per stack type (Node/TS vs Go) across every project, so CI behaves identically everywhere regardless of which project it's in."
metadata:
  status: planned
---

# CI/CD Consistency (planned)

## Problem this is meant to solve

Right now CI setup gets reinvented (or skipped) per project. This skill
should generate the same GitHub Actions shape for a given stack type
every time: lint → typecheck/build → test → (optionally) deploy trigger,
with the same job names and same failure behavior across every repo that
uses this stack.

## Scope (draft — refine before building)

- One workflow template per stack the builder actually uses: Node/TS
  (MERN-style), Go. Not a generic "works for anything" template — two
  concrete, opinionated ones.
- Consistent job/step naming across both, so switching between projects
  doesn't mean relearning what a failed check means.
- Explicitly NOT deploying itself — hands off to whatever
  `deployment-consistency` defines as the pre/post-deploy checklist, or
  to the platform's own deploy hook (Vercel git integration, Render
  auto-deploy).

## Before building

- Decide the actual required checks per stack (does Go CI need `go vet`
  + `staticcheck`? does the Node side need a specific lint config the
  builder already standardizes on?).
- Check whether this should read `AGENTS.md`'s conventions (from
  `project-scaffolder`) to know what "lint clean" and "typecheck clean"
  mean for this specific project, instead of hardcoding assumptions.

## Structure (matches project-scaffolder's pattern)

```
cicd-consistency/
├── SKILL.md
├── templates/       — .github/workflows/*.yml templates, one per stack type
└── references/      — notes on why each job/step exists, so future edits don't silently drop a check
```
