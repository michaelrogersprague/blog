# michaelrsprague.com

Source for my personal site and blog, built with [Eleventy](https://www.11ty.dev/) and hosted on Cloudflare Pages.

## Running locally

```
npm install
npm start        # dev server with live reload at http://localhost:8080
npm run build    # production build into _site/
```

## Layout

| Path | What it is |
| --- | --- |
| `content/index.md` | Home page: About plus the latest three posts |
| `content/artifacts.md` | Papers, patents and other writing |
| `content/blog/` | Blog posts, one Markdown file each |
| `content/blog.njk` | Blog index listing every post |
| `public/` | Copied to the site root as-is (e.g. `public/files/` → `/files/`) |
| `_data/metadata.js` | Site title, description, URL and author |
| `_includes/layouts/` | Page templates (`base.njk`, `post.njk`) |
| `css/index.css` | Site styles, including the background colour |
| `eleventy.config.js` | Eleventy plugins and settings |

## Writing a post

Add a Markdown file to `content/blog/`. The filename becomes the URL, so keep it lowercase (`my-post.md` → `/blog/my-post/`).

```markdown
---
title: My Post
description: One-line summary for search results and the feed.
date: 2026-11-21
tags: [physics]   # optional; creates /tags/physics/
draft: true       # optional; shows in `npm start` but not in builds
---
```

Images placed next to a post are automatically resized and converted to AVIF/WebP, and fenced code blocks get syntax highlighting.

## Deploying

Cloudflare Pages builds from `main`:

- Build command: `npm run build`
- Output directory: `_site`

Cloudflare Pages rejects any single file over 25 MiB.

## License

Based on [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog) (MIT, see `LICENSE`).
