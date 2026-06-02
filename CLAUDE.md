# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository. It is excluded from the public Jekyll build via `_config.yml` and is for internal use only.

## Project Overview

This is a Jekyll-based static website for the Massachusetts BioHub, live at `https://massbiohub.org`. The `CNAME` file and `_config.yml` are configured for this domain. `massbiohub.org` is currently registered at **Namecheap** (transferred from Wix in 2026); moving to Cloudflare Registrar is a long-term goal pending Namecheap's transfer-lock period.

**Naming convention.** Default to **"the BioHub"** throughout. Use **"WPI–MBI BioHub"** in places that need to emphasize the anchor partnership (About hero, Partners page intro, partner-facing copy). Don't use "WPI BioHub" alone — that under-credits MBI. Reserve "MassBioHub" for the brand/URL form only.

**Canonical partner URLs.** WPI → `https://www.wpi.edu/`, MBI → `https://mbi.bio/`, MassTech → `https://masstech.org/`. Use these consistently across footer and content pages.

**Hedging principle.** The BioHub has $5M MassTech funding (received Q1 2026), a Leadership Council, the BioLector hardware (commissioning), and the existing WPI CERES capabilities. It does **not yet have** the Pilot Facility, the Builder's Lab, the BioFoundry expansion, dedicated physical space beyond CERES, executed member contracts, or operational pilot fermentation. Default voice is forward-looking, present-state-honest: "will feature" not "features," "coming online over the next three years" not "operational," "designed to support" not "supports." If a page describes a capability without hedging, treat it as a bug.

## Build & Serve

```bash
# Build the site
jekyll build --future

# Serve locally with live reload
jekyll serve --future

# Build using Docker (matches CI)
docker run -v $PWD:/srv/jekyll jekyll/builder:latest jekyll build --future
```

There are no npm/pip dependencies — Jekyll is the only runtime dependency. `github-pages` (in the Gemfile) bundles `jekyll-sitemap`, which is enabled in `_config.yml`.

## Deployment

Pushing to `main` triggers the GitHub Actions workflow (`.github/workflows/jekyll-docker.yml`), which builds the site. Deployment is handled by GitHub Pages directly from `main`. Output goes to `_site/` (gitignored). If the live site looks different from local preview after a push, do a hard refresh (`Ctrl+Shift+R`) to clear the browser cache.

## Architecture

Content flows through three layers:

**Data** (`_data/`) → YAML files drive dynamic page sections:
- `nav.yml` — Navigation order: **Home · Services · Work With Us · Partners · About**
- `partners.yml` — Partner cards rendered on `partners.md`
- `news.yml` — Dormant; `news.md` is `published: false` until news exists to post (scheduled-task reminder runs monthly)

**Layouts** (`_layouts/`) → `page.html` extends `default.html` (root HTML shell with nav/footer). `default.html` contains canonical link, Open Graph / Twitter cards, `Organization` JSON-LD, and a skip-to-content link.

**Includes** (`_includes/`) → Reusable components: `nav.html`, `footer.html`, `partner-card.html`, `news-item.html` (dormant).

Content pages use Markdown with Jekyll frontmatter. Each page should set its own `description:` for SEO; the layout falls back to `site.description` if missing.

## Page map

| Route | File | Purpose |
|---|---|---|
| `/` | `index.md` | Lead paragraph → CTAs → By the numbers → What we're building (outcome cards) → Who we work with (persona cards) |
| `/about/` | `about.md` | Mission, vision, Why now, Where we sit, How we're funded, Who we serve, Engagement model, Leadership, Governance |
| `/services/` | `services.md` | Outcome-anchored sections: Scale your process · Engineer your strain · Train your team. Each section pairs current capabilities (CERES) with planned infrastructure (Pilot Facility, BioFoundry, Builder's Lab) wrapped in `<details>` blocks |
| `/work-with-us/` | `work-with-us.md` | Persona routing: Startup founder · Industry partner · Researcher/educator · Job seeker · Following along. Each ends in the same pre-filled `mailto:` |
| `/partners/` | `partners.md` | Anchor partner cards (WPI, MBI, MassTech) from `_data/partners.yml`. Network expansion is a planned addition once vetted |
| `/contact/` | `contact.md` | Single pre-filled `mailto:` CTA, Gateway Park / Builder's Lab addresses, "not sure who to talk to?" pointer to Work With Us |

## Design System

### Colors
All colors are defined as CSS variables in `style.css`:

| Variable | Value | Usage |
|---|---|---|
| `--header-bg` | `#2A6F8A` | Header background |
| `--accent` | `#1E5271` | Links, hover states |
| `--crimson` | `#AC2B37` | Primary buttons, `.mission` card background, focus outlines |
| `--bg` | `#FFFFFF` | Page background |
| `--bg2` | `#EAF2F5` | Card backgrounds, footer |
| `--line` | `#C8DDE5` | Borders |
| `--fg` | `#3d5261` | Body text, headings |
| `--muted` | `#466879` | Secondary text (darkened from #527A8A for WCAG AA) |

### Typography
Google Fonts are loaded in `_layouts/default.html`:
- **Plus Jakarta Sans** (400–800) — body text, navigation, all general content
- **League Spartan** (600) — site title in the header only, `font-size: clamp(22pt, 5vw, 34pt)`

### Cards
`.card` uses `--bg2` (pale teal) background with dark text. When used as a link, it is an `<a>` element with hover styling (`a.card:hover`); plain `<div class="card">` instances do not change on hover. `.person-photo` styles portrait images: square crop, `max-width/max-height: 260px`, rounded corners.

`.mission` — crimson background, white text, centered, italic body text. Used on `about.md` for the BioHub Mission Statement card. Contains an `<h2>` and `<p>`; use raw HTML (not Markdown) inside it.

`.card-centered-list` — modifier class for `.card` that centers card content while keeping `<ul>` items left-aligned. Used on the "Our engagement model" and Governance cards in `about.md`.

When using Markdown syntax (headings, bold, bullet lists) inside a `<div>`, always add `markdown="1"` to the div attribute.

### Accessibility
- Skip-to-content link is visually hidden until focused
- `:focus-visible` outlines applied site-wide
- Cookieless analytics (Goatcounter) — no banner required, but the footer notes the choice

## SEO / metadata
- `<title>`, `<meta description>`, OG tags, Twitter cards, and canonical link generated from page frontmatter in `default.html`
- `Organization` JSON-LD includes address, logo, and `sameAs` partner URLs
- `jekyll-sitemap` plugin generates `/sitemap.xml`; `robots.txt` references it
- Internal docs (`CLAUDE.md`, `SITE_PLAN.md`, `AUDIT.md`, `LICENSE`, `Gemfile*`) are listed under `exclude:` in `_config.yml` so they never become public pages

## Adding Content

- **New news item**: Add to `_data/news.yml` and remove `published: false` from `news.md` (and add News back to `_data/nav.yml`/footer if you want it linked)
- **New partner**: Add to `_data/partners.yml` — renders automatically on `/partners/`
- **New team member**: Add a card to the Leadership section in `about.md`; place portrait in `assets/img/people/`
- **New page**: Create a `.md` file with frontmatter `layout: page`, `title:`, `description:`, `permalink:`; add to `_data/nav.yml` if it should appear in the nav

## Known cleanup items

- `facilities.md` — content moved to `services.md`; the old file is `published: false` and should be removed with `git rm facilities.md`
- `_site/` was previously committed and is now `.gitignore`d — run `git rm -r --cached _site/` to untrack the committed copy
- OG image is 847×630; a proper 1200×630 version is a nice-to-have
- Leadership card photos for Jon Weaver and Liaohai Chen are still missing
