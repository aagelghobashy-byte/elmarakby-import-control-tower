# ElMarakby Import Control Tower

Static single-page operations control tower for import shipments, ACID/NAFEZA tracking, customs, documents, suppliers, costs, actions, and audit governance.

## Run locally

From this folder:

```bash
python3 -m http.server 8000 --bind 0.0.0.0
```

Then open `http://localhost:8000`.

Opening `index.html` directly also works. Data is persisted in the browser using `localStorage`; when running inside Manus, the Manus storage adapter is used automatically.

## Deploy to external hosting

Upload the contents of this folder to the document root / public directory of any static hosting service. No build step, server runtime, database, or environment variables are required.

Examples of compatible targets:

- Any cPanel / Apache / Nginx static document root
- Netlify Drop or a Netlify static site
- Cloudflare Pages
- GitHub Pages
- Amazon S3 static website hosting

The entry point is `index.html`.

## Important data note

This is a browser-local application. Each user/browser keeps its own operational data in `localStorage`. Use the built-in full backup/export controls before clearing browser data or changing devices. For shared multi-user data, a backend database and authenticated API would need to be added.
