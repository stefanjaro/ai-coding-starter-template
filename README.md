# AI-First Web App Agent Scaffold

Reusable GitHub template repository for guiding Codex and other coding agents while building web apps.

This is an **agent governance scaffold**, not a React, Next.js, Supabase, or framework starter. It contains concise instructions, situational guidance, and decision records that help agents build maintainable, secure, production-capable apps without bloating the context window.

## Use This In A New Project

1. Copy these files into the root of a new repo.
2. Edit `AGENTS.md` for rules the agent must always know.
3. Fill in `agent-reference/stack-decisions.md` as soon as stack choices are known.
4. Use `agent-reference/` for situational guidance the agent should consult when relevant.
5. Add ADRs in `decisions/` only for major, expensive-to-reverse decisions.

Codex supports `AGENTS.md` files for repository guidance. In practice, `AGENTS.md` is commonly used as a README-style instruction file for coding agents: short, direct, and specific to the repo.

## What Goes Where

- `AGENTS.md`: always-on agent instructions, constraints, workflow, and pointer map.
- `agent-reference/`: concise situational guidance the agent should open only when relevant.
- `decisions/`: minimal ADRs for major choices that explain why, not how.
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
