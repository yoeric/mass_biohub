# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based static website for the Massachusetts BioHub, hosted on GitHub Pages at `https://yoeric.github.io/mass_biohub`.

## Build & Serve

```bash
# Build the site
jekyll build --future

# Serve locally with live reload
jekyll serve --future

# Build using Docker (matches CI)
docker run -v $PWD:/srv/jekyll jekyll/builder:latest jekyll build --future
```

There are no npm/pip dependencies — Jekyll is the only runtime dependency.

## Deployment

Pushing to `main` triggers the GitHub Actions workflow (`.github/workflows/jekyll-docker.yml`), which builds and deploys the site automatically. Output goes to `_site/` (not committed).

## Architecture

Content flows through three layers:

**Data** (`_data/`) → YAML files drive dynamic page sections:
- `nav.yml` — Navigation links
- `partners.yml` — Partner cards rendered on `partners.md`
- `news.yml` — News items rendered on `index.md` and `news.md`

**Layouts** (`_layouts/`) → `page.html` extends `default.html` (root HTML shell with nav/footer)

**Includes** (`_includes/`) → Reusable components: `nav.html`, `footer.html`, `news-item.html`, `partner-card.html`

Content pages (`index.md`, `about.md`, `facilities.md`, `partners.md`, `news.md`, `contact.md`) use Markdown with Jekyll frontmatter and reference includes/data directly via Liquid templating.

Styling is in `assets/css/style.css` (CSS variables + Grid layout, mobile breakpoint at 900px). Logo images are in `assets/img/`.

## Adding Content

- **New news item**: Add an entry to `_data/news.yml` — it appears automatically on the homepage and news page.
- **New partner**: Add an entry to `_data/partners.yml` — it appears on the partners page.
- **New page**: Create a `.md` file with frontmatter `layout: page`, `title:`, and optionally `subtitle:`, then add it to `_data/nav.yml`.
