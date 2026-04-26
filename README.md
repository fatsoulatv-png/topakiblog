# Topaki Blog (Jekyll source)

Static blog for **blog.topaki.gr**, built with Jekyll. GitHub Pages will
auto-build this on every push to `main` — no GitHub Actions needed.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## Deploy to GitHub Pages

1. Create a new GitHub repo (any name, e.g. `topaki-blog`).
2. Push this folder to the `main` branch.
3. Repo → Settings → Pages → Source: "Deploy from a branch" → `main` / `/ (root)`.
4. DNS at your registrar:
   `CNAME blog → <github-username>.github.io.`
5. Wait ~5–30 min for DNS + HTTPS provisioning.

## Add a new post

Drop a new file in `_posts/` named `YYYY-MM-DD-slug.md` with frontmatter:

```yaml
---
title: "Τίτλος του άρθρου"
date: 2026-05-01 09:00:00 +0300
category: kalokairines     # one of the slugs in _data/categories.yml
slug: my-new-post
image: /assets/images/posts/something.jpg
image_alt: "alt text"
excerpt_text: "Σύντομη περιγραφή για την κάρτα της λίστας."
---

Markdown content here.
```

Push → GitHub rebuilds in ~1 min.

## Tweak branding

Open `assets/css/style.css` — the CSS variables at the top control the
whole site (colors, fonts, spacing).

## Files

| Path                    | Purpose                              |
|-------------------------|--------------------------------------|
| `_config.yml`           | Jekyll settings                      |
| `Gemfile`               | Tells GH Pages which gem set to use  |
| `index.html`            | Blog list (homepage)                 |
| `_posts/*.md`           | The 12 blog posts                    |
| `_layouts/*.html`       | Page templates                       |
| `_includes/*.html`      | Header, footer, card partials        |
| `_data/categories.yml`  | Category definitions                 |
| `categories/*.html`     | Per-category index pages             |
| `assets/css/style.css`  | All site styles                      |
| `assets/images/`        | Logo + post hero images              |
| `CNAME`                 | Custom-domain marker (blog.topaki.gr)|
