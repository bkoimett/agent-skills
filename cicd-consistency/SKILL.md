---
name: cicd-consistency
description: Create or audit CI workflows so they run the project's real install, lint, typecheck, test, build, and security checks consistently.
---

# CI/CD consistency

## Procedure

1. Inspect repository tooling and package scripts.
2. Detect package manager, languages, workspace layout, and build targets.
3. Identify existing CI workflows.
4. Compare CI commands with local project commands.
5. Add or update only the workflows required.
6. Verify YAML and referenced commands.
7. Report coverage and remaining gaps.

## Decision rules

- Never invent scripts that do not exist.
- Prefer the repository's package manager.
- Reuse lockfiles and cache safely.
- Keep independent jobs parallel where useful.
- Do not add deployment to CI unless requested.
- Do not expose secrets in logs.

## Verification

Run local equivalents of CI commands whenever possible.
