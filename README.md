# Personal Site

Built with Jekyll. Zero JS. Minimal dependencies.

## Local development

```bash
# Install dependencies
gem install bundler
bundle install

# Run locally (http://localhost:4000)
bundle exec jekyll serve --livereload
```

## Deploy to GitHub Pages

1. Create a repo named `yourusername.github.io` (or any name for project pages)
2. Push this directory to the `main` branch
3. Go to **Settings → Pages → Source**: select **GitHub Actions**
4. Push to `main` — the workflow in `.github/workflows/deploy.yml` handles the rest

## Custom domain

1. Buy your domain (Cloudflare Registrar is cheapest)
2. Add a `CNAME` file to the repo root with just your domain: `yourdomain.dev`
3. In your domain's DNS, add these A records pointing to GitHub Pages:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
4. In GitHub repo: **Settings → Pages → Custom domain** → enter your domain
5. Check "Enforce HTTPS" once DNS propagates (~10 min)

## Writing a new post

Create a file in `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
layout: post
title: "Your Post Title"
date: 2025-02-26
description: "One-line summary shown in the post list."
---

Your content here in Markdown.
```

## Customizing

- **Profile content**: edit `index.md`
- **Site title/URL/social handles**: edit `_config.yml`
- **Styles**: edit `assets/css/main.css`
- **Layout/nav**: edit `_layouts/default.html`
