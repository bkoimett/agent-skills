# AGENTS.md

## CRITICAL RULES

- Keep responses concise.
- Read the smallest relevant scope before acting.
- Never guess when repository evidence can answer the question.
- Use sub-agents for independent research, implementation, and review.
- Never duplicate detailed instructions from project documentation or skill references.
- Never add paid dependencies without approval.
- Never introduce a framework or change architecture without approval.
- Never claim success without verification.

## SKILL AUTHORING

- Keep `SKILL.md` focused on workflow and decisions.
- Put detailed, reusable knowledge in `references/`.
- Keep provider-specific guidance separate from general principles.
- Prefer inspection of the target repository over assumptions.
- Skills should be composable and safe to run independently.
- Read only the references relevant to the current task.

## VERIFICATION

Every implementation skill must define:
- what to inspect
- what commands/checks to run
- what successful completion means
- what to report

## GIT

Do not commit or push unless the user explicitly requests it.
