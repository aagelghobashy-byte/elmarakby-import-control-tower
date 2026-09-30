# Go-Live Readiness Checklist

## Current decision

**Do not use the GitHub Pages release as the shared production system of record yet.** It is suitable for controlled single-user operation, workflow review, demonstrations and UAT preparation. Shared production use is blocked until server-side persistence, authentication, authorization, evidence storage, server-enforced gates and tamper-resistant audit are implemented.

## Safe use of the current release

Before a controlled session:

- Use one named browser profile for the responsible operator.
- Confirm the correct release URL and date.
- Export a full JSON backup before starting and at the end of the session.
- Do not enter passwords, API keys or payment details.
- Treat the dashboard as an operational view, not as an authoritative database.
- Verify critical values against the source documents and ERP/customs records.
- Mark any manually entered or unverified integration information as pending in the operational notes.
- Do not delete or factory-reset data without a verified backup.

At the end of a session:

- Export the full backup JSON.
- Store it in an approved controlled location with the date, operator and release identifier.
- Record unresolved ACID, document, customs, cost and exception items in the approved business process.
- Confirm the next action and owner outside the browser-local tool until shared workflow controls exist.

## Pilot entry criteria

A 10-shipment pilot may begin only when the business owner confirms:

- The pilot records are explicitly marked TEST/UAT.
- A backup and restore rehearsal has been completed.
- The responsible operator understands that browser storage is local to the browser/device.
- No regulatory or financial submission is made solely from this tool.
- Source evidence is available outside the browser-local record.

## Production entry criteria

All of the following must be evidenced before production approval:

- Shared database with migrations and recovery procedure.
- Authentication and server-side RBAC/segregation of duties.
- Server-side validation, gate evaluation and controlled status transitions.
- Evidence upload, versioning, access control and retention.
- Append-only audit trail with actor, timestamp, action, before/after and correlation ID.
- Integration adapters tested against approved NAFEZA/CargoX/customs endpoints, or clearly labelled manual workflow.
- Automated unit, integration and end-to-end tests.
- Backup, restore and disaster-recovery drill.
- UAT sign-off from Operations, Compliance/Customs, Finance and IT/security.
- Rollback and incident procedures.

## Release labels

Use these labels precisely:

- **IMPLEMENTED:** present in the current code.
- **TESTED:** exercised by a repeatable technical check.
- **VALIDATED:** confirmed against the intended business behavior/evidence.
- **MOCKED:** simulated or manual; not an external integration.
- **PLANNED:** approved future work not present in the release.
- **NOT IMPLEMENTED:** absent from the release.
