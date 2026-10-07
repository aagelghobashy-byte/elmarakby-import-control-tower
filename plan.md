# Shareable Release Notes Website

## Goal
Create a standalone, static release-notes page from `CHANGELOG.md` that is easy to share with operations, QA and stakeholders while leaving the existing Import Control Tower runtime unchanged.

## Design direction
- **Movement:** Editorial operations brief / steel-industry control room.
- **Principles:** High legibility, calm hierarchy, evidence-first content and fast scanning.
- **Color philosophy:** Navy anchors trust, teal marks verified/operational improvements, amber marks releases and actions, and restrained red marks known gaps or attention items.
- **Layout:** A two-column editorial timeline with a persistent summary rail on wide screens and a single reading column on mobile.
- **Signature elements:** Release number rail, status chips, and a compact “what changed / what stayed” split.
- **Interaction:** Filtering is immediate and reversible; every release card can be expanded without navigation.
- **Animation:** Minimal entrance fade and subtle hover lift only; no distracting loops.
- **Typography:** System sans stack for Arabic/English readability, monospace for dates, versions and metadata.
- **Brand essence:** A trustworthy release brief for teams operating the Al-Marakby import control tower. Personality: precise, calm, accountable.
- **Voice:** “See what changed. Know what stayed protected.” / “A clear release trail for operational confidence.”

## Implementation
- Add `release-notes.html` as a self-contained static page.
- Represent the changelog entries as structured data in the page script for filtering and summaries.
- Preserve a direct link to the live control tower and the source `CHANGELOG.md`.
- Do not alter `index.html`, browser data, workflows or existing modules.
- Publish the new page through the existing GitHub Pages branch.

## Project structure
- `index.html` — existing operational application; unchanged.
- `release-notes.html` — new shareable release-notes website.
- `CHANGELOG.md` — source record.
- `docs/` — existing operational documentation.
