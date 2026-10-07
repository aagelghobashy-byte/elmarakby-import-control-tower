# Change Log

## 2026-10-08 — Mixed-direction presentation pass

### Improved

- Kept the Arabic interface shell, navigation and labels right-to-left.
- Set shipment tables, SLA tables, identifiers, dates, values, search fields and operational form values to left-to-right reading order.
- Improved tracker stage-detail alignment while keeping the Arabic timeline structure intact.
- Added mobile table overflow behavior so wide operational data remains readable without collapsing columns.

### Preserved

- Existing records, workflows, navigation, browser persistence and all data operations.

## 2026-10-05 — Color contrast review

### Improved

- Increased contrast for secondary text, small labels, table headings and form placeholders.
- Refined status colors for ACID, ETA, action and document states so they remain clear on light backgrounds.
- Strengthened secondary, success, warning and neutral button colors.
- Preserved luminous but readable accent colors in dark mode.

### Preserved

- Existing data, workflows, controls, storage behavior and navigation.

## 2026-10-05 — Visual clarity and presentation polish

### Improved

- Unified the visual language around a clear steel operations palette: navy, teal, amber and controlled status colors.
- Strengthened contrast for headers, navigation, KPI cards, tables, forms, alerts and Control Center surfaces.
- Added focused input states, zebra rows, clearer table headers, stronger section hierarchy and more legible action buttons.
- Refined responsive behavior for tablet and mobile widths.
- Corrected dark-theme surfaces so cards, notices and alerts remain readable without bright white blocks.

### Preserved

- All data, JavaScript workflows, navigation, storage behavior and existing controls.

## 2026-10-05 — Control Center and data operations expansion

### Added

- New **Control Center** tab for centralized operation and administration.
- Controlled editor for existing shipment supplier, description, origin, ETA, value, entity, mode, priority, pipeline stage, ACID state, ACID number and remarks.
- Data health check for duplicate IDs, missing suppliers, invalid values, inconsistent ACID records and invalid stages.
- Centralized JSON backup/restore, CSV exports, shipment entry template download, module control board and UI preference reset.
- Arabic operating guide at `docs/CONTROL_CENTER_GUIDE.md`.

### Preserved

- Existing shipment, supplier, ACID, gate, document, customs, GRN, cost, action and audit workflows.
- Existing browser persistence, archive behavior and protected destructive-operation confirmations.

## 2026-10-02 — Clear Control Tower v2

### Added

- New **Operational Pulse** strip on the Dashboard with live counts for ACID attention, ETA overdue, open actions and incomplete document packs.
- Pulse cards are actionable: ACID attention opens the existing ACID filter, Actions opens Action Center, and Document Packs opens Documents.
- Default presentation is now the clearer light enterprise theme while preserving a saved dark preference.

### Improved

- Reworked visual hierarchy, surface contrast, spacing, panel headers, KPI cards, navigation, buttons, tables and responsive behavior.
- Removed the previous overly decorative treatment in favor of calm Steel Group navy, teal, amber, green and red state semantics.
- Preserved all existing shipment records, modules, handlers, storage and workflows.

## 2026-10-01 — Live preview and visual clarity refresh

### Updated

- Refined the color system for stronger readability and clearer operational states.
- Improved dashboard spacing, KPI cards, navigation, form fields, buttons and table rows.
- Preserved all current modules, event handlers, data structures and workflows.
- Corrected light-theme backgrounds, borders, placeholders and text contrast after live preview validation.

### Verified

- Navigation to New Shipment and Shipment Tracker.
- Shipment selection and 12-stage tracker rendering.
- Dashboard shipment search and entity filtering.
- Dark/light theme toggle.
- HTML structure and JavaScript syntax.

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
