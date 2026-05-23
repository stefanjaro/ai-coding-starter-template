# Dependency Policy

Dependencies are long-term maintenance commitments. Add them only when they reduce real complexity or provide trusted integration coverage.

## Add Criteria

Before adding a dependency, confirm:

- It solves a current problem, not a speculative one.
- The package is actively maintained.
- The license is acceptable for the project.
- The bundle/runtime cost is reasonable.
- The API is stable enough for production use.
- The security posture fits the feature risk.
- The project does not already have an equivalent dependency.

## Preferences

- Prefer official SDKs for platform integrations.
- Prefer well-maintained packages with clear ownership.
- Prefer small focused packages over broad frameworks when the project already has structure.
- Prefer standard library or existing app utilities when they are sufficient.

## Major Dependencies

Ask or clearly justify before adding:

- Frameworks
- ORMs or database clients
- Auth libraries
- Payment libraries
- Rich text editors
- State management libraries
- Build tooling
- Large UI systems

## Updates

- Keep lockfiles consistent.
- Review changelogs for major version changes.
- Run relevant tests after updates.
- Note breaking changes in the PR description.

## Removal

- Remove unused dependencies when safely verified.
- Remove related config, imports, tests, and docs.
- Run dependency and test checks after removal.
