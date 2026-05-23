# Stack Decisions

Each project must explicitly choose its stack. The agent must initialize and maintain this file as the project evolves.

When stack, hosting, backend, auth, database, analytics, payments, or architectural decisions become known or change, update this file before continuing implementation.

Do not casually switch stack choices mid-project. Record why a switch is necessary and create an ADR if it is expensive to reverse.

## Default Recommendation

Prefer a managed backend first, such as Supabase or Convex, unless the project has a clear reason not to.

## Current Choices

- Frontend: TBD
- Backend: TBD
- Database: TBD
- Auth: TBD
- Hosting: TBD
- Payments: TBD
- Analytics: TBD
- Email: TBD

## Architecture Notes

- Primary app shape: TBD
- Data ownership boundaries: TBD
- Server/client split: TBD
- Background jobs: TBD
- File storage: TBD

## Change Rules

- Update this file before implementing a newly known stack choice.
- Keep entries short: decision, reason, relevant constraints.
- Link to ADRs for major decisions.
- Do not use this file as an architecture manual.
