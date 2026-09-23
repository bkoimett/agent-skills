# Review verification

Run the project's existing checks. Prefer:

1. Syntax/config validation
2. Focused tests
3. Lint/typecheck
4. Build
5. Integration or smoke tests

Do not substitute a generic command when the repository defines a different one.

If the project has project-scaffolder-generated documents (AGENTS.md, DESIGN.md, WORKFLOW.md, README.md), reference those as the ground truth for what the project foundation should look like. Verify that the documents exist, use uppercase filenames, and contain project-specific information rather than generic placeholders.