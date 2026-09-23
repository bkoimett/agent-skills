# Agent Skills

A focused collection of reusable skills for AI coding agents.

## Skills

- `project-scaffolder` - turn requirements into a verified project foundation; generates `AGENTS.md`, `DESIGN.md`, `WORKFLOW.md`, `README.md` at the project root
- `code-conventions` - audit and maintain project conventions
- `cicd-consistency` - create and audit consistent CI
- `deployment-consistency` - standardize deployment workflows
- `project-standards-audit` - inspect existing projects for canonical startup documents, verify structure against project-scaffolder standards, create missing documents, and return an audit report
- `app-review` - create/updates the persistent `REVIEW.md` documentation artifact and returns a concise human-readable review summary; does not modify application source code, configuration, dependencies, or runtime behavior

## Design

Skills are intentionally narrow. `SKILL.md` contains the workflow and references contain detailed, provider- or stack-specific guidance.

The intended lifecycle is:

New project
  → project-scaffolder
  → Existing project onboarding / maintenance
  → project-standards-audit
  → app-review
  → CI/CD
  → Deployment
