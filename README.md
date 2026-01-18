# Employment Background

Static Astro site for a resume-style employment background + evolving portfolio.

## Current implemented state

- Full resume/portfolio layout rendered at `/` (default).
- Alternate routes:
	- `/minimal` for a minimal “Dirk-only” view (useful for layout debugging).
	- `/resume` for an explicit full-resume route (currently same as `/`).
- Page entries live in `src/pages/*.astro` and wrap `src/layouts/Layout.astro`.
- Main resume content: `src/components/Welcome.astro` (resume-style sections + placeholders + sidebars).
- No integrations, API/server routes, or content collections configured.

### Placeholder content conventions

- Resume PDF: put a file in `public/` (e.g. `public/resume.pdf`) and pass `resumeUrl="/resume.pdf"`.
- Optional preview image: put `public/resume.png` and pass `resumeImageUrl="/resume.png"`.

## Commands

Run from the repo root:

- Install: `npm install`
- Dev server: `npm run dev` (default `http://localhost:4321`)
- Production build: `npm run build` (outputs `dist/`)
- Preview build: `npm run preview`

Tip: `npm run dev` hot-reloads automatically when you save files. `npm run build` just generates `dist/` (it does not serve), and `npm run preview` serves the built output.

## Repo notes

- Astro config: `astro.config.mjs`
- TypeScript: strict config via `astro/tsconfigs/strict` (see `tsconfig.json`)

## Docs

- Ideas/backlog: `docs/portfolio-sections-ideas.md`
- Progress log: `docs/progress-log.md`

## Workflow notes (GitHub)

- No CI is configured in this repo; run `npm run build` before pushing/merging.
- If using PRs: keep changes on feature branches and use PR review for anything non-trivial.
- Track notable changes in `docs/progress-log.md`.
