# Decision Records

Use minimal ADRs for major decisions that are expensive to reverse.

ADRs explain **why** a decision was made. They do not replace implementation docs, tickets, or code comments.

## When To Create One

- Stack or hosting choice
- Database or auth model
- Major architecture boundary
- Payment or billing model
- Migration strategy with lasting consequences
- Security-sensitive tradeoff

## When Not To Create One

- Routine implementation detail
- Small refactor
- Bug fix
- Naming choice
- Temporary workaround that will be removed soon

## Rules

- Keep each ADR short enough to scan in one screen.
- Use `000-template.md`.
- Prefer numbered filenames: `001-short-title.md`.
- Mark superseded decisions instead of rewriting history.
