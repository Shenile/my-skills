# my-skills

Personal agent toolkit for Shenile.

This repo holds custom skills I reuse across agentic IDEs and CLIs (Cursor, Claude Code, Windsurf, Codex, and anything else I mount an agent with). It is not a product library. It is a portable set of instructions so every agent I work with can pick up the same workflows.

## What lives here

Each skill is a self-contained folder with a `SKILL.md` (and extra files when a skill needs scripts, templates, or examples). Agents that support skills load those files and follow them when the task matches.

```
skills/
  <skill-name>/
    SKILL.md          # when to use it, and how to run it
    ...               # optional scripts, templates, references
```

Skills are the source of truth. Tool-specific config (Cursor rules, Claude project files, and so on) should point here instead of duplicating the same playbook.

## Mounting this toolkit

Clone the repo somewhere stable, then point the agent at `skills/`.

```bash
git clone https://github.com/Shenile/my-skills.git
```

Typical options:

- **Cursor** — clone into the user skills directory, or add this repo as a project the agent can read. Prefer loading from `skills/` rather than copying files into `.cursor/` unless the IDE requires it.
- **Claude Code / other CLIs** — clone locally and register the `skills/` path in that tool’s skill or plugin config.
- **Any other agentic IDE** — clone, then add `skills/` to the agent’s extra context / knowledge / skills path.

The goal is the same everywhere: one clone, one set of skills, mounted wherever I am working.

## Adding a skill

1. Create `skills/<skill-name>/SKILL.md`.
2. Start the file with a short description of **when** the agent should use it.
3. Write the procedure in the order the agent should follow. Keep it concrete: commands, file paths, output shape, and stop conditions.
4. Put reusable scripts or templates next to `SKILL.md` in the same folder.
5. Mention the skill in the list below.

Keep names kebab-case (`review-pr`, `cut-release`). One skill, one job.

## Skill index

None yet. Skills land in `skills/` as they are written.

## Notes

- Treat this as private operating procedure even if the GitHub repo is public. Do not put secrets, tokens, or machine-specific credentials in skill files.
- Prefer small, composable skills over one giant playbook.
- If an IDE cannot load skills natively, paste or `@`-mention the relevant `SKILL.md` for that session.
