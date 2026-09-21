# agent-skills

Personal collection of agent skills for keeping full-stack work (MERN, Go,
TypeScript) consistent across projects — deployed on Vercel, Render, and
Docker. Built for and tested with [opencode](https://opencode.ai), listed
on [skills.sh](https://skills.sh).

## Install a skill

```bash
npx skills add bkoimett/agent-skills --skill <skill-name>
```

Or grab the whole collection:

```bash
npx skills add bkoimett/agent-skills
```

## Skills

| Skill | Status | What it does |
|---|---|---|
| [`project-scaffolder`](./project-scaffolder) | **Ready** | Reads an existing `PRD.md` and generates `design.md`, `AGENTS.md`, `WORKFLOW.md`, and `README.md` for a new project, cross-referenced and slop-checked. |
| [`cicd-consistency`](./cicd-consistency) | Planned | Same GitHub Actions workflow pattern per stack type (Node/TS, Go), across every project. |
| [`deployment-consistency`](./deployment-consistency) | Planned | Platform-agnostic pre/post-deploy checklist (Vercel, Render, Docker) so a deploy means the same thing everywhere. |
| [`code-conventions`](./code-conventions) | Planned | Enforces the lint config, commit style, and README structure that `project-scaffolder` establishes, catching drift over time. |

## Why these four

Scaffolding, CI, deployment, and code conventions are the four places a
solo/small-team builder's work quietly drifts between projects. Each skill
is scoped narrow on purpose — one job, done consistently — rather than
one large "best practices" skill that tries to cover everything
generically.

## Structure

Each skill folder is self-contained:

```
<skill-name>/
├── SKILL.md          — what the skill does and how the agent should use it
├── templates/         — the actual template files it fills in
└── references/        — supporting guidance (e.g. avoid-ai-slop.md)
```
