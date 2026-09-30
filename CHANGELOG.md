# Change Log

## 2026-09-30 — Readiness and forensic audit pass

### Preserved

- Existing single-page dashboard and all current tabs.
- Existing client-side shipment, ACID, gate, document, customs, supplier, cost, action and audit workflows.
- Existing GitHub Pages deployment and public URL.
- Existing data format and browser storage behavior.

### Added

- `docs/FORENSIC_AUDIT.md` — evidence-based architecture map, traceability map and gap classification.
- `docs/GO_LIVE_READINESS.md` — safe-use, pilot and production-entry criteria.
- `docs/USER_GUIDE.md` — operator workflow and backup guidance.

### Not changed

- No runtime HTML/CSS/JavaScript behavior.
- No existing data records.
- No repository architecture migration.
- No claims that the current release is a shared production system of record.

### Known blocking gaps

- Browser-local persistence only.
- No server-side authentication/RBAC/SoD.
- No server-enforced gates or immutable audit.
- No evidence object storage/versioning.
- No verified external NAFEZA/CargoX/customs API integration.
- No automated test suite.
