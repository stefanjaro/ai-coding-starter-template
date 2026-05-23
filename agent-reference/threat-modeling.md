# Threat Modeling Guidance

Use this for auth, authorization, payments, webhooks, file handling, external integrations, personal data, secrets, admin features, or cross-tenant behavior.

## Scope

- Identify the feature or system being changed.
- List sensitive assets: secrets, personal data, payment or entitlement data, business-critical records, and provider payloads.
- Identify trust boundaries: browser/server, server/database, app/provider, user/admin, tenant/tenant, and public/private routes.
- Name the actors: legitimate users, admins/operators, external services, and likely attackers.

## Threats To Check

- Unauthorized reads, writes, deletes, exports, or privilege escalation.
- Cross-tenant or cross-user data exposure.
- Client-side trust where server-side enforcement is required.
- Missing webhook signature verification or non-idempotent webhook handling.
- Secret, token, stack trace, provider payload, or personal data leakage.
- Unsafe file uploads, downloads, parsing, or path handling.
- Replay, duplicate processing, race conditions, or inconsistent entitlement state.
- Overbroad service-role, admin, or background-job access.

## Controls

- Enforce authorization at the server or database layer.
- Use narrow database policies and test sensitive access paths.
- Validate and normalize untrusted input at boundaries.
- Verify external provider signatures and store provider event IDs.
- Make webhook and background processing idempotent.
- Redact sensitive data from logs and user-facing errors.
- Prefer platform-managed auth and official SDKs for security-sensitive integrations.

## Verification

- Add regression tests for identified threats when practical.
- Include negative authorization tests for sensitive resources.
- Run relevant checks and repeat the fix/check loop until they pass or a blocker remains.
- Summarize residual risk when a threat is accepted rather than fully eliminated.
