---
name: deployment-consistency
description: Audit and standardize deployment workflows, environments, configuration, health checks, and rollback procedures for supported deployment targets.
---

# Deployment consistency

## Procedure

1. Identify the application and deployment target.
2. Inspect existing deployment configuration.
3. Identify required environment variables and secrets.
4. Validate build and start commands.
5. Validate health checks and smoke tests.
6. Check rollback or recovery procedure.
7. Report gaps before making destructive changes.
8. Apply requested deployment changes.
9. Verify the deployed application.

## Decision rules

- Provider-specific behavior belongs in references.
- Never invent environment variable values.
- Never print secrets.
- Never run destructive production commands without explicit approval.
- Prefer reversible deployment changes.
- Deployment success requires post-deploy verification.
