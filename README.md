# Clan Site

Static site built with [Astro](https://astro.build), deployed via Netlify.

## Editing site info

Clan name and tagline live in [`src/site-config.ts`](src/site-config.ts) — edit those two strings first.

## Posting an update

Add a new Markdown file to `src/content/updates/`, e.g.:

```markdown
---
title: Tournament this Saturday
date: 2026-08-16
summary: One-line summary shown in the feed list.
---

Full write-up goes here in Markdown.
```

Commit and push — Netlify rebuilds and deploys automatically. Posts are sorted newest-first by the `date` field, no other config needed.

## Commands

| Command           | Action                                      |
| :----------------- | :------------------------------------------- |
| `npm install`       | Install dependencies                         |
| `npm run dev`       | Start local dev server at `localhost:4321`   |
| `npm run build`     | Build production site to `./dist/`           |
| `npm run preview`   | Preview the production build locally         |

## Deploying (Netlify)

1. Push this repo to GitHub.
2. In Netlify, "Add new site" → "Import an existing project" → pick the repo.
3. Build command `npm run build`, publish directory `dist` (already set in `netlify.toml`).
4. Every push to the main branch auto-deploys.
