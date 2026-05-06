# Tasteful Frontend Designer

This repository contains one reusable agent skill: [`SKILL.md`](./SKILL.md).

Use it when you want an AI coding agent to produce frontend work with stronger visual design, spacing, typography, responsiveness, accessibility, and polish.

## What This Repo Includes

- `SKILL.md`: the skill definition and operating instructions

## How To Load It

### Codex or Any Agent With Skill File Support

1. Clone this repository or copy `SKILL.md`.
2. Place `SKILL.md` in the agent's skills directory, or in the location your tool expects for local skills.
3. Reference or enable the skill by name: `tasteful-frontend-designer`.
4. Ask for frontend work normally. The skill should activate for UI-related tasks.

## Other AI Agents

If your agent does not support skill files directly:

1. Open [`SKILL.md`](./SKILL.md).
2. Copy the contents into the agent's system prompt, custom instructions, project instructions, or rules file.
3. Save the configuration.
4. Start your frontend task and tell the agent to follow the `tasteful-frontend-designer` guidance.

## Add To `AGENTS.md`

If your workflow uses an `AGENTS.md` file, add this note:

```md
## Frontend Design Quality

For any frontend, UI, UX, landing page, dashboard, form, app screen, or component work, use the `tasteful-frontend-designer` skill before implementing. Prioritize polished visual design, hierarchy, spacing, typography, responsive behavior, accessibility, and reusable components.
```

## Example Setups

### Claude Projects

- Paste the contents of `SKILL.md` into the project's custom instructions.
- Keep the file in the repo so the instructions can be updated and reused.

### Cursor Rules or Project Instructions

- Copy the guidance from `SKILL.md` into your workspace rules or project instructions.
- Use it for UI tickets, redesigns, landing pages, dashboards, and component work.

### Any Prompt-Driven Agent

- Attach or paste `SKILL.md` before the task.
- Tell the agent to prioritize visual hierarchy, tasteful styling, responsive behavior, and accessible states.

## Suggested Prompt

```text
Use the tasteful-frontend-designer skill for this task. Keep the UI cohesive, polished, responsive, and accessible. Avoid generic styling decisions.
```

## Updating The Skill

Edit [`SKILL.md`](./SKILL.md), then reload or re-paste it into whatever agent environment you use.
