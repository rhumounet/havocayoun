# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project purpose

Showcase website for a French lawyer specializing in criminal law ("droit pénal"), family law ("droit de la famille"), and drug-related cases ("affaires de stupéfiants"). The site is currently a blank Astro starter and will be built out from scratch.

## Commands

```sh
npm run dev      # Start dev server at localhost:4321
npm run build    # Build production site to ./dist/
npm run preview  # Preview production build locally
npx astro check  # Type-check .astro files
```

## Architecture

[Astro 6](https://astro.build) with strict TypeScript. File-based routing: every `.astro` file in `src/pages/` becomes a URL route.

Key conventions:
- `src/layouts/` — shell HTML wrappers; pages compose layouts via `<slot />`
- `src/components/` — reusable `.astro` components imported into pages/layouts
- `src/assets/` — images/SVGs imported directly into components (processed at build time)
- `public/` — static files served as-is (favicons, fonts, etc.)

Astro components use a frontmatter fence (`---`) for server-side TypeScript followed by the HTML template. Styles written inside a `<style>` block are scoped to the component by default.
