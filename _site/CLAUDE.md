# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based static website for the Massachusetts BioHub, live at `https://massbiohub.org`. The `CNAME` file and `_config.yml` are already configured for this domain.

Canonical partner URLs: WPI → `https://www.wpi.edu/`, MBI → `https://mbi.bio/`, MassTech → `https://masstech.org/`. Use these consistently across footer and content pages.

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

Pushing to `main` triggers the GitHub Actions workflow (`.github/workflows/jekyll-docker.yml`), which builds and deploys the site automatically. Output goes to `_site/` (not committed). If the live site looks different from local preview after a push, do a hard refresh (`Ctrl+Shift+R`) to clear the browser cache.

## Architecture

Content flows through three layers:

**Data** (`_data/`) → YAML files drive dynamic page sections:
- `nav.yml` — Navigation links (Facilities was renamed to Services, permalink `/services/`)
- `partners.yml` — Partner cards rendered on `partners.md`
- `news.yml` — News items rendered on `index.md` and `news.md`

**Layouts** (`_layouts/`) → `page.html` extends `default.html` (root HTML shell with nav/footer)

**Includes** (`_includes/`) → Reusable components: `nav.html`, `footer.html`, `news-item.html`, `partner-card.html`

Content pages (`index.md`, `about.md`, `facilities.md`, `partners.md`, `news.md`, `contact.md`) use Markdown with Jekyll frontmatter and reference includes/data directly via Liquid templating.

Styling is in `assets/css/style.css` (CSS variables + Grid layout, mobile breakpoint at 900px). Images are organized into `assets/img/logos/` (biohub, wpi, mbi, techhub logos) and `assets/img/people/` (portrait photos).

## Design System

### Colors
All colors are defined as CSS variables in `style.css`:

| Variable | Value | Usage |
|---|---|---|
| `--header-bg` | `#2A6F8A` | Header background, primary buttons |
| `--accent` | `#1E5271` | Links, hover states |
| `--crimson` | `#AC2B37` | Latest News (`hero-card`) background |
| `--bg` | `#FFFFFF` | Page background |
| `--bg2` | `#EAF2F5` | Secondary backgrounds (hero card, footer) |
| `--line` | `#C8DDE5` | Borders |
| `--fg` | `#3d5261` | Body text, headings |
| `--muted` | `#527A8A` | Secondary text |

### Typography
Google Fonts are loaded in `_layouts/default.html`:
- **Plus Jakarta Sans** (400–800) — body text, navigation, all general content
- **League Spartan** (600) — site title ("The BioHub") in the header only, `font-size: 34pt`
- **Lexend** (600) — loaded but not currently applied; available for use

### Cards
`.card` uses `--bg2` (pale teal) background with dark text and is a clickable `<a>` element. `.hero-card` uses `--crimson` background with white text for the Latest News section.

## Page Notes

**`index.md`** — single-column layout: lead paragraph → CTA buttons → "What we do" cards (3-column grid, each links to `/services/`) → Latest News (`hero-card`). Title is "Building with Biology" with subtitle "Driving the Bioindustrial Manufacturing Revolution in Central Massachusetts".

**`about.md`** — plain Markdown: Mission → Who we serve → Our engagement model → Lead Partner Websites. Title is "About Us" (no subtitle). No cards or HTML blocks.

**`contact.md`** — "Get in touch" section uses a `.cards` grid. Dr. Eric M. Young's card (`young_burn_50.jpg`, `.person-photo` class) links via `mailto:` — email address is intentionally not shown in text to prevent scraping. Jon Weaver's card has no email. Collaboration inquiries section lists what to include when reaching out.

## Adding Content

- **New news item**: Add an entry to `_data/news.yml` — it appears automatically on the homepage and news page.
- **New partner**: Add an entry to `_data/partners.yml` — it appears on the partners page.
- **New page**: Create a `.md` file with frontmatter `layout: page`, `title:`, and optionally `subtitle:`, then add it to `_data/nav.yml`.
