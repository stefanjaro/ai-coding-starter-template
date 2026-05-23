# Data Access Guidance

Use this when adding or changing persistence, ownership, authorization, sharing, imports, exports, or multi-user behavior.

## Core Questions

- What data is created, read, updated, deleted, imported, or exported?
- Who owns each record: user, team, organization, admin, system, or external provider?
- Who can read, write, share, archive, restore, or delete it?
- Which fields are sensitive, personal, financial, or security-relevant?
- What must never be exposed to clients, logs, analytics, or third-party services?

## Authorization Rules

- Enforce authorization server-side or at the database layer.
- Prefer database-level policies such as RLS when the stack supports them.
- Deny by default when ownership or tenant boundaries are unclear.
- Check ownership, role, tenant, status, and feature entitlement before reads or writes.
- Keep admin and service-role paths separate from user-facing request paths.
- Add tests for sensitive read/write boundaries and negative cases.

## Data Correctness

- Validate untrusted input at the boundary before persistence.
- Normalize data before storage when it prevents duplicate or ambiguous records.
- Preserve audit-relevant timestamps and actor IDs for important state changes.
- Make destructive operations explicit, reversible, or soft-delete when product needs are unclear.
- Treat imports, backfills, and migrations as data changes that need verification.

## Privacy And Exposure

- Return only fields the caller needs.
- Avoid leaking existence of private records through errors, counts, search, or timing-sensitive flows.
- Redact personal data, secrets, tokens, provider payloads, and payment details from logs.
- Document retention, deletion, and export behavior when handling personal or business-critical data.

## Before Implementation

- Identify data ownership and access rules before writing handlers, policies, or schema changes.
- Update `agent-reference/stack-decisions.md` if the data model introduces a new architectural boundary.
- Use `agent-reference/threat-modeling.md` for sensitive data, external services, payments, or cross-tenant access.
