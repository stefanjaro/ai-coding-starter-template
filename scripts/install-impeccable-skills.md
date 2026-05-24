# Install Impeccable Design Skills

Do not run this from the scaffold template automatically.

Use this when a project needs stronger frontend design guidance for avoiding generic AI-looking UI, overused purple gradients, nested-card layouts, weak typography, and other common visual anti-patterns.

## Recommended Install

Run this inside the target project:

```sh
npx skills add pbakaus/impeccable
```

This installs the Impeccable skill for supported AI coding harnesses, including Codex.

To refresh later:

```sh
npx impeccable skills update
```

## Manual Install

If the `skills` installer is unavailable, visit <https://impeccable.style/#downloads>, download the bundle for your agent tool, and extract it into the target project.

For a Codex install copied from the upstream repository:

```sh
git clone https://github.com/pbakaus/impeccable.git
cd impeccable
```

For a project-local Codex install:

```sh
cp -r dist/agents/.agents /path/to/your-project/
mkdir -p /path/to/your-project/.codex
cp -r dist/codex/.codex/agents /path/to/your-project/.codex/
```

For a user-wide Codex install:

```sh
mkdir -p ~/.agents/skills
cp -r dist/agents/.agents/skills/* ~/.agents/skills/
mkdir -p ~/.codex
cp -r dist/codex/.codex/agents ~/.codex/
```

Restart Codex if the skill does not appear. In Codex, open `/skills` or use `$impeccable`.

## Optional Anti-Pattern Check

Impeccable also provides a detector for common design anti-patterns:

```sh
npx impeccable detect src/
```

Refresh from the upstream project or `npx impeccable skills update` rather than manually editing vendored skill files.
