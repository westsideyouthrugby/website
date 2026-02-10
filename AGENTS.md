# Westside Youth Rugby — Site Guide for AI Coding Agents

## Stack

- **Hugo** static site generator (extended edition, v0.154+)
- **PaperMod** theme (git submodule at `themes/PaperMod/`)
- **GitHub Pages** hosting via GitHub Actions

## Build Commands

- `hugo server` — local dev server at localhost:1313
- `hugo --minify` — production build to `public/`

## Content Structure

```
content/
  _index.md          # homepage (front matter only, PaperMod homeInfoParams drives display)
  about.md           # about page
  contact.md         # contact page
  news/
    _index.md        # news section listing
    YYYY-MM-DD-*.md  # news posts
```

## Adding a News Post

Create `content/news/YYYY-MM-DD-slug.md`:

```markdown
---
title: "Post Title"
date: YYYY-MM-DD
summary: "Brief description."
---

Post body here.
```

## Configuration

- `hugo.yaml` — site config (theme, menus, PaperMod params)
- Do NOT edit files in `themes/PaperMod/` directly

## Deployment

Push to `main` triggers `.github/workflows/hugo.yaml` which builds and deploys to GitHub Pages.

## Images

Place images in `static/img/`. Reference in content as `/img/filename.png`.
