# Tadashi — Notes & Observations

A local-first personal blog built with Astro. The design uses a warm paper-and-walnut palette with moss green accents, content collections for articles, static category routes, client-side search, and a responsive editorial layout.

## Development

Install dependencies once:

```sh
npm install
```

Start Astro in background mode:

```sh
npm run astro -- dev --background
```

Manage the background server with:

```sh
npm run astro -- dev status
npm run astro -- dev logs
npm run astro -- dev stop
```

Build the static site with:

```sh
npm run build
```

## Writing a post

Articles are Markdown files in `src/data/blog/`. Copy an existing post and update its frontmatter:

```yaml
---
title: "Post title"
description: "A short summary for cards and search."
pubDate: 2026-11-18
category: "Field Notes"
readTime: "4 min read"
featured: false
tone: "hills"
---
```

The available artwork tones are `hills`, `workbench`, `window`, `ink`, `garden`, and `walk`. Article and category routes are generated automatically during the build.

## Newsletter behavior

This is a local-only build, so the newsletter form provides a complete confirmation interaction and stores the submitted address in browser local storage. Connect the form to an email provider before deploying it publicly.
