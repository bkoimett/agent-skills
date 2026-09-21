---
name: deployment-consistency
description: "NOT YET BUILT. Planned: a pre-deploy checklist enforced the same way regardless of target platform (Vercel, Render, Docker, GitHub Actions) — env var parity across environments, migration-before-deploy ordering, health-check verification, rollback steps."
metadata:
  status: planned
---

# Deployment Consistency (planned)

## Problem this is meant to solve

Deploys drift between projects because each one's checklist lives in the
builder's head, not in a file the agent reads. This skill should make
"what has to be true before I call this deployed" the same shape across
every project, even when the platform underneath (Vercel vs Render vs
Docker) is different.

## Scope (draft — refine before building)

- A platform-agnostic pre-deploy checklist: env vars present in the
  target environment, migrations applied before the new code that needs
  them, a smoke test / health check run after deploy, a known rollback
  step.
- Platform-specific adapters underneath the same checklist shape — e.g.
  "confirm preview vs production env vars aren't crossed" means something
  concrete on Vercel and something different on Render/Docker, but the
  checklist item itself is the same across projects.
- Explicitly NOT trying to be a CI/CD pipeline generator — that's
  `cicd-consistency`'s job. This skill is the pre-flight and post-flight
  check around whatever pipeline already exists.

## Before building

- Pull the actual deploy checklist from 2-3 of the builder's real
  projects (NyumbaPro, Serenity Place, the ecommerce project) and look
  for what's actually repeated versus what's genuinely platform-specific.
- Decide whether this reads `design.md`'s "Environments" section (from
  `project-scaffolder`) as its source of truth, so the two skills stay
  connected instead of duplicating environment info.

## Structure (matches project-scaffolder's pattern)

```
deployment-consistency/
├── SKILL.md
├── templates/       — the checklist template(s), one per platform adapter
└── references/      — platform-specific notes (Vercel quirks, Render quirks, Docker quirks)
```
