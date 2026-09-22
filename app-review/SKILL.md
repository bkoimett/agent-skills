---
name: app-review
description: Perform a read-only application review covering security, SEO, AI discoverability, accessibility, configuration, tests, and documentation drift.
---

# App review

## Purpose

Find concrete risks and inconsistencies before release.

## Procedure

1. Identify application type and deployment target.
2. Read relevant project documentation.
3. Inspect authentication and authorization.
4. Inspect secrets and configuration handling.
5. Check common web security risks.
6. Check SEO and crawlability where applicable.
7. Check AI discoverability and machine-readable documentation where applicable.
8. Check accessibility and core user paths for UI applications.
9. Compare documentation with actual behavior.
10. Run available tests, lint, typecheck, and builds.
11. Produce a prioritized factual report.

## Decision rules

- Review is read-only by default.
- Do not invent vulnerabilities.
- Distinguish confirmed findings from recommendations.
- Include evidence and affected files/routes.
- Do not rank the project overall.

## References

Load only the references relevant to the application.
