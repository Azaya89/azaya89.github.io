# azaya89.github.io

Personal portfolio site — built with [Quarto](https://quarto.org) and hosted on GitHub Pages.

## Structure

```
azaya89.github.io/
├── _quarto.yml          # Site config, nav, theme
├── index.qmd            # Landing page
├── about.qmd            # Work history, skills, contact
├── projects/
│   └── index.qmd        # Project showcase
├── blogs/
│   └── index.qmd        # Blog listings
│   └── posts/           # Add individual posts here
├── assets/
│   ├── styles.css       # Custom CSS
│   └── images/          # Static assets
└── docs/                # Rendered output (auto-generated, do not edit)
```

## Local development

```bash
# Preview site with live reload
quarto preview

# Render to docs/
quarto render
```

## Deploying

This site deploys to GitHub Pages via Quarto's built-in publish command:

```bash
quarto publish gh-pages
```

This renders the site and force-pushes the output to the `gh-pages` branch.
GitHub Pages is configured to serve from that branch.

## Adding a blog post

1. Create a folder under `blogs/posts/your-post-slug/`
2. Add an `index.qmd` with YAML front matter:

```yaml
---
title: "Post Title"
date: YYYY-MM-DD
description: "One sentence summary shown in the listing."
---
```

3. Run `quarto preview` to check it locally, then `quarto publish gh-pages` to deploy.
