# Copilot instructions (employmentBackground)

## Project snapshot
- Astro 5 static site starter (no integrations configured yet). Config: [astro.config.mjs](../astro.config.mjs)
- Source lives in [src/](../src/): pages in [src/pages/](../src/pages/), layouts in [src/layouts/](../src/layouts/), components in [src/components/](../src/components/)
- Uses strict TypeScript settings via `astro/tsconfigs/strict`: [tsconfig.json](../tsconfig.json)

## Dev workflows (use npm scripts)
- Install: `npm install`
- Dev server (default `http://localhost:4321`): `npm run dev`
- Production build (outputs `dist/`): `npm run build`
- Preview built site: `npm run preview`
- Astro CLI passthrough: `npm run astro -- <args>`

## Code patterns used here
- `.astro` files use the frontmatter block for imports/logic, then template markup.
  - Example page imports layout + component: [src/pages/index.astro](../src/pages/index.astro)
  - Layout provides `<slot />` for page content: [src/layouts/Layout.astro](../src/layouts/Layout.astro)
- Assets are imported as modules and referenced via `.src`.
  - Example: `import background from '../assets/background.svg'` then `src={background.src}`: [src/components/Welcome.astro](../src/components/Welcome.astro)

## Conventions to follow when editing
- Keep the current structure: page → layout wrapper → components.
- Prefer local component CSS via `<style>` blocks inside `.astro` files (as in the starter).
- Preserve ESM (`"type": "module"`) conventions; use `import`/`export` (see [package.json](../package.json)).

## What’s intentionally NOT here (yet)
- No tests, linters, or formatters configured.
- No content collections, server routes, or framework integrations present.

## Safe change strategy
- When refactoring, update imports in [src/pages/index.astro](../src/pages/index.astro) and any referenced components/layouts.
- If you replace the starter “Welcome” content, do it by editing [src/components/Welcome.astro](../src/components/Welcome.astro) and/or swapping the component used in [src/pages/index.astro](../src/pages/index.astro).
