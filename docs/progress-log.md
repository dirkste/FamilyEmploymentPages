# Progress log

Small, factual record of notable changes to this site/repo.

## 2026-01-17

- Built a resume-style single-page layout in `src/components/Welcome.astro` and wired it from `src/pages/index.astro`.
- Added portfolio section ideas backlog: `docs/portfolio-sections-ideas.md`.
- Adopted a feature-branch + PR workflow (with review feedback handled via `gh`).
- Updated docs (README + backlog) to reflect current site state.

## 2026-01-18

- Restored `/` to render the full resume view (after temporarily pointing it at a minimal debugging page).
- Added explicit routes for A/B comparison: `/minimal` (minimal) and `/resume` (full).
- Improved the center resume preview “paper” presentation in `src/components/Welcome.astro`.
