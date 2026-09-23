# Documentation audit procedures

## Scope

Audit the project's canonical startup documents and related artifacts for compliance with project standards and consistency.

## Checklist

### Canonical startup documents

- [ ] `AGENTS.md` exists at project root
- [ ] `DESIGN.md` exists at project root
- [ ] `WORKFLOW.md` exists at project root
- [ ] `README.md` exists at project root
- [ ] All filenames use uppercase (e.g., `AGENTS.md`, not `agents.md`)
- [ ] No conflicting lowercase duplicates exist without migration

### Document content review

- Read each existing startup document.
- Check for consistency with the project's actual stack and structure.
- Verify that generated content matches project-scaffolder standards.
- Look for signs of documentation drift (claims that contradict actual behavior).

### Lowercase duplicate handling

- If a lowercase variant (e.g., `agents.md`, `readme.md`) exists alongside the canonical uppercase document:
  1. Read the lowercase variant.
  2. If it contains unique or useful information not in the canonical document, migrate it.
  3. After migration, remove or rename the lowercase duplicate.
  4. If the lowercase variant is identical to the canonical document, remove it.

### Project structure

- Inspect the project directory tree.
- Verify that the project structure is consistent with what project-scaffolder would generate.
- Flag unnecessary package boundaries or missing directories that should exist per the stack.

### Verification

- Run the project's existing lint, typecheck, test, and build commands.
- Report any failures or warnings.
- Do not substitute generic commands when the repository defines different ones.

## Output

Record findings per document. Distinguish observed facts from potential issues and recommendations. Use the audit-report template for the final report.