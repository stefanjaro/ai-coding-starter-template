# Skill Preferences

Use this when the user asks an agent to create or update a skill.

## Defaults

- Use intuitive names that clearly describe the workflow.
- Keep frontmatter lean: `name` and `description` only unless another config is truly needed.
- Keep the skill as small as the workflow allows.
- Prefer concrete step sequences over broad guidance.

## What Skills Are For

Skills should capture a preferred sequence of steps:

- How to approach a recurring task.
- Which tools or checks to run, and in what order.
- What output shape the user expects.
- What project-specific pitfalls affect that workflow.

## What Skills Are Not For

Do not create a skill only to store context. Put context in:

- `user-docs/` for user-authored plans, PRDs, long prompts, and background material.
- `agent-reference/` for concise agent-facing project guidance.

Exception: include context in a skill only when it directly affects the sequence of steps described by that skill.

## Before Creating A Skill

- Confirm the request is a repeatable workflow, not just background information.
- If the user only wants to capture context, recommend `user-docs/` or `agent-reference/` instead.
- If both workflow and context are needed, keep the skill procedural and link to the context doc.
