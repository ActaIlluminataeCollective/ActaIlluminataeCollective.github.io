# Research collective site

Static site for **Arin**, **Noah**, **Hershil**, and **Andrei** to publish papers and notes. Built with [Eleventy](https://www.11ty.dev/) (Markdown → HTML).

## Run locally

1. Install [Node.js](https://nodejs.org/) 20+.
2. In this folder: `npm install` then `npm start` (opens a local preview with live reload).
3. Production build: `npm run build` (output in `_site/`).

## Add a new article

1. Create `src/posts/YYYY-MM-DD-short-title.md`.
2. Start the file with front matter:

```yaml
---
title: "Your title"
author: "Name"
abstract: "One line for the listing (optional but nice)."
date: 2026-04-12
---
```

3. Write the rest in Markdown below the second `---`.
4. Commit and push. If GitHub Actions is enabled, the live site updates after the workflow finishes.

You can copy `src/posts/2026-04-02-reading-notes-template.md` as a starting point.

## GitHub Pages

1. Push this repository to GitHub (this folder as the repo root).
2. **Settings → Pages → Build and deployment**: source **GitHub Actions**.
3. Edit `.github/workflows/pages.yml` and set `BASE_PATH` to `/<your-repo-name>/` (with slashes).  
   Example: repo `research-collective-site` → `BASE_PATH: /research-collective-site/`.  
   For a **user** site (`username.github.io` with site at the domain root), use `BASE_PATH: /`.
4. Optionally update `url` in `src/_data/site.json` to match your real GitHub Pages URL.

## Customize

- Global title, tagline, authors: `src/_data/site.json`
- Colors and typography: `src/assets/css/main.css`
