# Westside Youth Rugby — Site Guide for AI Coding Agents

## Stack

- **Hugo** static site generator (extended edition, v0.154+)
- **PaperMod** theme (git submodule at `themes/PaperMod/`)
- **GitHub Pages** hosting via GitHub Actions

## Build Commands

- `hugo server` — local dev server at localhost:1313
- `hugo --minify` — production build to `public/`
- `prek run --all-files` — lint (yamllint, whitespace, YAML checks); CI runs this before the build, and `pre-commit run --all-files` works if `prek` is not installed

## Content Structure

```
content/
  _index.md          # homepage (front matter only, profileMode drives display)
  photos.md          # photos page, images in static/img/photos/
```

The homepage is controlled entirely by `profileMode` in `hugo.yaml`. The `_index.md` file only carries SEO metadata (`description`).

## Configuration

- `hugo.yaml` — site config (theme, menus, PaperMod params)
- Homepage uses PaperMod `profileMode` (image, title, subtitle, buttons)
- Custom CSS overrides live in `assets/css/extended/custom.css`
- Do NOT edit files in `themes/PaperMod/` directly

## Deployment

Push to `main` triggers `.github/workflows/hugo.yaml` which builds and deploys to GitHub Pages.

## Images

Place images in `static/img/`. Reference in content or config as `/img/filename.png`.

The site logo is `static/img/logo.png`.

## Local Testing

1. Run `hugo server` and open `http://localhost:1313/`
2. Verify: logo centered, title displayed, subtitle with contact link, Rugby Oregon button links to rugbyoregon.com, Photos button opens `/photos/`
3. Run `prek run --all-files` to confirm lint passes
4. Run `hugo --minify` to confirm production build succeeds with no errors
