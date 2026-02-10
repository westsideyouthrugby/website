# Westside Youth Rugby

Website for Westside Youth Rugby, a community rugby club in Portland, OR.

Built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. Hosted on GitHub Pages.

## Local Development

Requires Hugo extended edition (v0.154+).

```sh
hugo server
```

Open http://localhost:1313 to preview the site.

## How to Add a News Post

1. Go to the `content/news/` folder in this repo on GitHub
2. Click **Add file** → **Create new file**
3. Name it `YYYY-MM-DD-short-description.md` (e.g., `2026-03-15-spring-registration.md`)
4. Paste this template:

```markdown
---
title: "Your Post Title"
date: YYYY-MM-DD
summary: "A one-line summary."
---

Write your post content here. You can use **bold**, *italic*, and [links](https://example.com).
```

5. Click **Commit changes** at the bottom
6. The site will rebuild and deploy automatically within a few minutes

## How to Edit a Page

1. Navigate to the file in `content/` (e.g., `content/about.md`)
2. Click the pencil icon to edit
3. Make your changes and commit

## Where to Put Images

1. Upload images to the `static/img/` folder
2. Reference them in content as `![Alt text](/img/filename.png)`

## Custom Domain (Future)

To add a custom domain:

1. **DNS records** — Add A records pointing to GitHub Pages IPs:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
2. **CNAME** — Add a CNAME record for `www` pointing to `<org>.github.io`
3. **GitHub Settings** — Go to repo Settings → Pages → Custom domain, enter your domain
4. **SSL** — GitHub auto-provisions a Let's Encrypt certificate
5. **Config** — Update `baseURL` in `hugo.yaml` to your new domain

## Project Structure

```
hugo.yaml                    # site configuration
content/                     # all site content (Markdown)
  _index.md                  # homepage
  about.md                   # about page
  contact.md                 # contact page
  news/                      # news section
    _index.md                # news listing page
    YYYY-MM-DD-slug.md       # individual posts
static/                      # static assets (images, etc.)
themes/PaperMod/             # theme (git submodule — do not edit)
.github/workflows/hugo.yaml  # CI/CD workflow
```
