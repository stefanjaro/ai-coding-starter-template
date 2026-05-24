# AI-First Web App Agent Scaffold

Reusable GitHub template repository for guiding Codex and other coding agents while building web apps.

This is an **agent governance scaffold**, not a React, Next.js, Supabase, or framework starter. It contains concise instructions, situational guidance, and decision records that help agents build maintainable, secure, production-capable apps without bloating the context window.

## Use This In A New Project

Use this scaffold before the app has a real shape. The goal is to turn a rough idea into shared project context, stack decisions, and a phased implementation plan before the coding agent starts making large choices on your behalf.

1. Copy this template into a new repo.
2. Add a markdown file for your idea in `user-docs/`.
3. Ask your coding agent to pressure-test and refine the idea. For example:

   ```text
   Tell me what I might be missing. Tell me the things I don't know I don't know so we can refine and build upon this idea further. Tell me what you think is necessary for the MVP stage and what we can do later, especially if we're in a hurry to get this into the hands of a few users so we can iterate based on real user feedback.
   ```

4. Ask the agent to update the idea file with the refined context.
5. Ask the agent to fill in the Project Context placeholders in `AGENTS.md`.
6. Discuss the right tech stack for the idea, including backend, auth, database, hosting, payments, analytics, email, file storage, and any privacy or security constraints.
7. Install project-specific agent skills once the stack is known. Common examples:

   ```sh
   npx skills add pbakaus/impeccable
   npx skills add supabase/agent-skills
   ```

   Install Supabase skills only for projects that use Supabase. For UI-heavy projects, run Impeccable's project-teaching flow after installation so the design guidance has product context.
8. Ask the agent to update `agent-reference/stack-decisions.md` and any relevant `AGENTS.md` guidance with the chosen stack and constraints.
9. Ask the agent to run the `implementation-plan` skill against the idea document to create `user-docs/implementation-plan/index.md` and phase files.
10. Review the generated plan, tighten scope, and make sure the first phase has user-verifiable acceptance criteria.
11. Start building one phase at a time. For example:

   ```text
   Execute phase 01.
   ```

During implementation, ask the agent to keep the active phase file updated with progress notes, verification results, blockers, and any material divergences from the original plan.

Codex supports `AGENTS.md` files for repository guidance. In practice, `AGENTS.md` is commonly used as a README-style instruction file for coding agents: short, direct, and specific to the repo.

## What Goes Where

- `AGENTS.md`: always-on agent instructions, constraints, workflow, and pointer map.
- `agent-reference/`: concise situational guidance the agent should open only when relevant.
- `decisions/`: minimal ADRs for major choices that explain why, not how.
- `user-docs/`: idea docs, PRDs, project notes, prompts, and implementation plans.
- `user-docs/implementation-plan/`: phased MVP plan, phase statuses, progress notes, and divergence log.
- `scripts/`: setup notes and one-off project instructions.

## Editing Guidance

Edit `AGENTS.md` when the rule must apply to every agent task. Keep it short and high-signal.

Edit `agent-reference/` when guidance is conditional, stack-specific, or only useful for some tasks.

Use `decisions/` when a choice is costly to reverse or affects future implementation. Do not create ADRs for routine implementation details.

## Supabase Agent Skills

Supabase agent skills can be installed separately using Supabase's official skills package:

```sh
npx skills add supabase/agent-skills
```

Do this inside projects that actually use Supabase. Do not vendor Supabase skills into this scaffold; refresh them from the official source.
