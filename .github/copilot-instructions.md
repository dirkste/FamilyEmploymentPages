# Copilot instructions (employmentBackground)

## Project snapshot
- Astro 5 static site (no integrations/server routes/content collections). Config: [astro.config.mjs](../astro.config.mjs)
- Routes are file-based:
  - `/` → [src/pages/index.astro](../src/pages/index.astro) renders [src/components/Welcome.astro](../src/components/Welcome.astro)
  - `/resume` → [src/pages/resume.astro](../src/pages/resume.astro) (currently same content as `/`)
  - `/minimal` → [src/pages/minimal.astro](../src/pages/minimal.astro) renders [src/components/Minimal.astro](../src/components/Minimal.astro) for layout/debug
- Layout wrapper is [src/layouts/Layout.astro](../src/layouts/Layout.astro) (provides `<slot />` + `<title>`).
- TypeScript is strict via `astro/tsconfigs/strict`: [tsconfig.json](../tsconfig.json)

## Dev workflows
- Install: `npm install`
- Run locally: `npm run dev` (defaults to `http://localhost:4321`)
- Build: `npm run build` (outputs `dist/`)
- Preview build: `npm run preview`
- VS Code debug config: “Development server” in [.vscode/launch.json](../.vscode/launch.json)

## Repo conventions (Astro)
- Keep the structure: page → layout wrapper → components (see [src/pages/index.astro](../src/pages/index.astro)).
- Component data is co-located with rendering in frontmatter (typed arrays + `.map()` loops), especially in [src/components/Welcome.astro](../src/components/Welcome.astro).
- Define props as a `type Props` and destructure from `Astro.props as Props` (see [src/components/Minimal.astro](../src/components/Minimal.astro)).
- Prefer component-scoped styling via `<style>` in the `.astro` file (Layout/Welcome/Minimal all do this).

## Assets + resume placeholders
- Static files live in `public/` and are referenced by absolute paths (e.g. `/resume.pdf`).
- `Welcome.astro` supports:
  - `resumeUrl="/resume.pdf"`
  - `resumeImageUrl="/resume.png"`
  (see the Props docstrings in [src/components/Welcome.astro](../src/components/Welcome.astro)).

## Safe change strategy
- If changing routes/content, update the page entrypoints under [src/pages/](../src/pages/) and keep them wrapped in [src/layouts/Layout.astro](../src/layouts/Layout.astro).
- Use `/minimal` ([src/pages/minimal.astro](../src/pages/minimal.astro)) as a quick smoke-test for layout/CSS changes.
- No CI configured; run `npm run build` before merging/pushing.
