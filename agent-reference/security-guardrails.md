# Security Guardrails

Use this checklist when implementing auth, data access, payments, webhooks, file handling, logging, or external integrations.

## Secrets

- Keep secrets server-side only.
- Never commit real secrets, tokens, private keys, or `.env` values.
- Use project-approved secret storage in deployed environments.
- Treat public client environment variables as non-secret.

## Auth

- Prefer platform-managed auth over custom auth.
- Validate session state on the server for protected actions.
- Do not trust client-side route guards as authorization.

## Authorization

- Enforce authorization at the server/data layer.
- Check ownership, role, tenant, and status before reads or writes.
- Deny by default when ownership is unclear.

## Database Policies

- Use database-level authorization such as RLS where applicable.
- Keep policies narrow and testable.
- Add policy tests for sensitive tables.
- Avoid service-role access in user-facing request paths.

## Input Validation

- Validate untrusted input at boundaries.
- Prefer schema validation shared by handlers and tests.
- Normalize before persistence when useful.

## Errors

- Return safe error messages to users.
- Do not leak stack traces, SQL details, tokens, or provider payloads.
- Log enough context to debug without exposing sensitive data.

## Logging

- Redact secrets, credentials, payment data, and personal data.
- Avoid logging full request bodies by default.
- Use stable event names for security-relevant actions.

## Dependencies

- Review dependency health before adding packages that touch auth, crypto, parsing, uploads, payments, or server execution.
- Prefer official SDKs for security-sensitive integrations.

## Payments And Webhooks

- Verify webhook signatures.
- Make webhook handlers idempotent.
- Store provider event IDs.
- Do not grant entitlements until payment state is verified server-side.
