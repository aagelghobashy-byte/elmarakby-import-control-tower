# ElMarakby Import Control Tower

Static single-page operations control tower for import shipments, ACID/NAFEZA tracking, customs, documents, suppliers, costs, actions, and audit governance.

## Current release status

This release is **UAT-ready as a controlled single-user browser tool** and is **not yet production-ready as a shared system of record**. It now includes a centralized Control Center for controlled shipment editing, health checks, portable backup/restore, CSV exports, entry templates, module shortcuts and preference management. The runtime still uses browser-local persistence, with a Manus storage adapter when available and a `localStorage` fallback elsewhere.

The current release does not provide server-side authentication, RBAC, database persistence, immutable evidence storage, server-enforced gates, or verified live NAFEZA/CargoX/customs integrations. Do not use it as the sole authoritative source for real regulatory, financial or shipment decisions until those controls are implemented and accepted.

## Permanent site

https://aagelghobashy-byte.github.io/elmarakby-import-control-tower/

Shareable release notes:

https://aagelghobashy-byte.github.io/elmarakby-import-control-tower/release-notes.html

## Documentation

- [Shareable release notes](release-notes.html)
- [Forensic audit and implementation map](docs/FORENSIC_AUDIT.md)
- [Go-live readiness checklist](docs/GO_LIVE_READINESS.md)
- [Operator user guide](docs/USER_GUIDE.md)
- [Control Center operating guide](docs/CONTROL_CENTER_GUIDE.md)
- [Change log](CHANGELOG.md)

## Run locally

From this folder:

```bash
python3 -m http.server 8000 --bind 0.0.0.0
```

Then open `http://localhost:8000`.

Opening `index.html` directly also works. Data is persisted in the browser using `localStorage`; when running inside Manus, the Manus storage adapter is used automatically.

## Deploy to external hosting

Upload the contents of this folder to the document root / public directory of any static hosting service. No build step, server runtime, database, or environment variables are required.

Compatible targets include GitHub Pages, Netlify, Cloudflare Pages, cPanel/Apache/Nginx static hosting and Amazon S3 static website hosting.

The entry point is `index.html`.

## Data and backup note

Each browser profile/device keeps its own operational data. Use the built-in full backup/export controls before clearing browser data, changing devices, importing a backup or making a major operational update. For shared multi-user data, a server-backed database, authentication and audited API layer are required.
