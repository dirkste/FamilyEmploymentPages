# Employment Background

Static Astro site for a resume-style employment background + evolving portfolio.

## Current implemented state

- Single-page resume/portfolio layout rendered at `/`.
- Page entry: `src/pages/index.astro` (wraps the layout + the main content component).
- Main content: `src/components/Welcome.astro` (resume-style sections + placeholders).
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
