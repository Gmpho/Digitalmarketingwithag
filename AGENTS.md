# Digital Marketing with AG

Astro v7 static site. Blog about SEO/GEO/AEO, social automation, and monetization.

## Commands

| Command | Action |
|---|---|
| `npm run dev` | Start dev server at `localhost:4321` |
| `npm run build` | Build static site to `dist/` |
| `npm run preview` | Preview built site |
| `npx astro check` | Run type checking |

Use `astro dev --background` to run in background mode; manage with `astro dev stop|status|logs`.

## Architecture

- **Framework**: Astro v7, static output (no SSR)
- **Styling**: Tailwind CSS v4 via `@tailwindcss/vite` plugin — uses `@import "tailwindcss"` in `global.css`, no `tailwind.config`
- **Dark mode**: Class strategy — `.dark` class on `<html>`, persisted in `localStorage('theme')`
- **React available**: `@astrojs/react` can be added via `npx astro add react` for interactive components
- **Content**: MDX blog posts at `src/content/blog/` with schema in `src/content.config.ts`
- **Content API**: Astro v7 collections (`glob()` loader, `render()` from `astro:content`, `.id` instead of old `.slug`)

## Content

Blog posts live in `src/content/blog/` as `.mdx` files. Required frontmatter:

```yaml
---
title: string
description: string
pubDate: date (YYYY-MM-DD)
tags: string[]
---
```

Dynamic routes via `src/pages/blog/[...slug].astro` — `slug` maps to the file's `.id`.

## Key Components

- `BaseLayout.astro` — All pages use this (nav, footer, SEO, theme toggle)
- `BlogLayout.astro` — Wraps blog post content with article header
- `SEO.astro` — Injects JSON-LD schema (`BlogPosting`/`WebSite`), OG tags, meta
- `BlogCard.astro` — Post preview card for listing page

## Pages

| Route | File |
|---|---|
| `/` | `src/pages/index.astro` |
| `/blog` | `src/pages/blog/index.astro` |
| `/blog/[slug]` | `src/pages/blog/[...slug].astro` |
| `/about` | `src/pages/about.astro` |
| `/contact` | `src/pages/contact.astro` |

## Environment

Copy `.env.example` to `.env` for local vars. Never commit `.env*` files (gitignored).

## Deploy

Build with `npm run build`, deploy `dist/` to Cloudflare Pages (or any static host). No server required.
