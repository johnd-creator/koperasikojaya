## Project Overview

The official KOJAYA landing page built with Astro 7 and deployed as static assets on Cloudflare Workers. Repository name: `koperasikojaya`.

`konsep.png` ("konsep" = concept) at the repo root is an 846×1860 design mockup — treat it as the visual reference for the landing page layout and match it when building sections.

## Development

Requires **Node >= 22.12.0** (enforced via `engines` in package.json).

When starting the dev server, use background mode:

```
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

## Commands

| Command | Action |
| :-- | :-- |
| `npm run dev` | Dev server at `localhost:4321` |
| `npm run build` | Production build to `./dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run astro check` | TypeScript + Astro diagnostics for `.astro` files (run after edits) |
| `npm run astro add <integration>` | Add integrations (e.g. `tailwind`, `react`) — none are installed yet |

## Architecture

Standard Astro static layout: `src/pages/*.astro` files become routes by filename, reusable sections live in `src/components/`, shared layouts in `src/layouts/`, and static assets in `public/`. Production output is generated in `dist/` and deployed with Wrangler.

TypeScript is in **strict** mode (`tsconfig.json` extends `astro/tsconfigs/strict`). Component-local styles use a `<style>` tag scoped per-component by default.

No CSS framework, UI framework, or content collections are configured. Add them via `astro add` rather than hand-editing `astro.config.mjs` and `package.json`.

## Conventions

- `CLAUDE.md` is a **symlink to this file** (`AGENTS.md`). Edit `AGENTS.md` only — both stay in sync. Do not create a separate `CLAUDE.md`.
- Commit messages are not yet established (no git history convention to follow).

## Documentation

Full documentation: https://docs.astro.build

Consult these guides before working on related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)
