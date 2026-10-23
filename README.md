# ICLP

A redesign concept for **Indian Constitutional Law & Philosophy**, Gautam Bhatia's blog on Indian constitutional law. It's a static site built with [Eleventy](https://www.11ty.dev/) and deployed on Netlify.

This is the first version of the project. A newer version lives at [arpit-agr/iclp-v2](https://github.com/arpit-agr/iclp-v2).

| Version | Live site |
| --- | --- |
| v1 (this repo) | [iclp-v1.netlify.app](https://iclp-v1.netlify.app) |
| v2 | [v2-iclp.netlify.app](https://v2-iclp.netlify.app) |

> [!NOTE]
> This is a personal design and front-end project. Post titles come from the original blog, but the post bodies are placeholder text.

## Features

- Light and dark themes, with a manual toggle
- Reading experience for long posts: table of contents, footnotes with back-links, inline asides, and estimated reading time
- Tag pages, pagination, and related-post suggestions
- RSS feed
- Generated Open Graph images for each page
- Privacy-friendly Twitter embeds
- Contact form handled by Netlify Forms
- Minified HTML and CSS inlined per page, with no client-side framework

## Tech stack

| Area | Tools |
| --- | --- |
| Static site generator | Eleventy 1.x, Nunjucks, Markdown (markdown-it) |
| Styling | Plain CSS, inlined and minified with clean-css |
| Fonts | Inter (self-hosted) |
| Hosting | Netlify, with `netlify-plugin-cache` |

## Getting started

You need [Node.js](https://nodejs.org/) installed.

```bash
npm install
```

To run a local dev server with live reload:

```bash
npm start
```

To build the site into `public/`:

```bash
npm run build
```

## Project structure

```
src/
├── _data/          # Global site data (site.json) and helpers
├── _includes/
│   ├── components/ # CSS, one file per component
│   ├── layouts/    # Base, page, post, and index layouts
│   ├── macros/     # Nunjucks macros
│   └── partials/   # Reusable template pieces
├── _11ty/filters/  # Custom Eleventy filters
├── pages/          # About, Contact, Tags, 404, and so on
├── posts/          # Blog posts, written in Markdown
├── scripts/        # Small client-side scripts (theme toggle, details)
├── fonts/
└── img/
.eleventy.js        # Eleventy config: plugins, filters, shortcodes, collections
netlify.toml        # Netlify build settings
```

### Writing a post

Add a Markdown file to `src/posts/` with front matter like this:

```markdown
---
title: "Post title"
date: "2021-10-13"
tags:
  - freedom of speech
---

Post content goes here.[^1]

[^1]: A footnote.
```

## Credits

- Content and concept: [Gautam Bhatia](https://indconlawphil.wordpress.com/), *Indian Constitutional Law & Philosophy*
- Design and development: [Arpit Agrawal](https://github.com/arpit-agr)
