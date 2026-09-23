---
name: app-review
description: Create/updates the persistent REVIEW.md documentation artifact and returns a concise human-readable review summary. Does not modify application source code, configuration, dependencies, or runtime behavior.
---

# App review

## Purpose

Create/updates the persistent `REVIEW.md` documentation artifact and returns a concise human-readable review summary. Does not modify application source code, configuration, dependencies, or runtime behavior. It creates or updates the persistent `REVIEW.md` documentation artifact.

## Procedure

1. Identify application type and deployment target.
2. Read relevant project documentation, including any project-scaffolder-generated startup documents (`AGENTS.md`, `DESIGN.md`, `WORKFLOW.md`, `README.md`).
3. Inspect authentication and authorization.
4. Inspect secrets and configuration handling.
5. Check common web security risks (see `app-review/references/owasp.md` and `app-review/references/security.md`).
6. Check SEO and crawlability where applicable (see `app-review/references/seo.md`).
7. Check AI discoverability and machine-readable documentation where applicable (see `app-review/references/ai-discoverability.md`).
8. Check accessibility and core user paths for UI applications.
9. Compare documentation with actual behavior (see `app-review/references/documentation-drift.md`).
10. Run available tests, lint, typecheck, and builds (see `app-review/references/verification.md`).
11. Create or update `REVIEW.md` at the project root with the review findings.
12. Return a concise human-readable review summary to the agent/user.

## Decision rules

- App review does not modify application source code, configuration, dependencies, or runtime behavior. It creates or updates the persistent `REVIEW.md` documentation artifact.
- Do not invent vulnerabilities.
- Distinguish confirmed findings from recommendations.
- Include evidence and affected files/routes.
- Do not rank the project overall.
- REVIEW.md creation or update is a mandatory output of the skill. The review is not complete until `REVIEW.md` has been successfully created or updated.

## References

Load only the references relevant to the application.
