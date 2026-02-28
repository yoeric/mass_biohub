# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based static website for the Massachusetts BioHub, hosted on GitHub Pages at `https://yoeric.github.io/mass_biohub`. The custom domain `massbiohub.org` is purchased and pending DNS setup — once configured, `_config.yml` `url` and `baseurl` should be updated to `https://massbiohub.org` and `""` respectively, and the `CNAME` file is already in place.

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

## Design System

### Colors
All colors are defined as CSS variables in `style.css`:

| Variable | Value | Usage |
|---|---|---|
| `--header-bg` | `#2A6F8A` | Header background, card backgrounds |
| `--accent` | `#1E5271` | Links, hover states |
| `--crimson` | `#AC2B37` | Primary CTA buttons (ties to WPI brand) |
| `--bg` | `#FFFFFF` | Page background |
| `--bg2` | `#EAF2F5` | Secondary backgrounds (hero card, footer) |
| `--line` | `#C8DDE5` | Borders |
| `--fg` | `#12283A` | Body text |
| `--muted` | `#527A8A` | Secondary text |

### Typography
Google Fonts are loaded in `_layouts/default.html`:
- **Plus Jakarta Sans** (400–800) — body text, navigation, all general content
- **League Spartan** (600) — site title ("The BioHub") in the header only
- **Lexend** (600) — loaded but not currently applied; available for use

### Cards
`.card` uses `--header-bg` (teal) background with white text. `.hero-card` uses `--bg2` (pale teal) for the Latest News section.

## Page Notes

**`index.md`** — single-column layout: lead paragraph → CTA buttons → "What we do" cards (3-column grid) → Latest News (`hero-card`)

**`about.md`** — plain Markdown: Mission → Engagement model → Who we serve → Lead Partner Websites. No cards or HTML blocks.

## Adding Content

- **New news item**: Add an entry to `_data/news.yml` — it appears automatically on the homepage and news page.
- **New partner**: Add an entry to `_data/partners.yml` — it appears on the partners page.
- **New page**: Create a `.md` file with frontmatter `layout: page`, `title:`, and optionally `subtitle:`, then add it to `_data/nav.yml`.
