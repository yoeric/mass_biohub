# Massachusetts BioHub website — design.md

**Audit method for this site.** Before proposing edits, build a claim inventory — file, line, claim, backing source, status (verified / stale / unsourced / contradicted) — and rank once from it. Verify against public sources in parallel (subagents); external checks caught the false NSF claim that reading the site had not. Report items already correct, not only problems. The ranked inventory lives in the ledger, not a new file.

## Brand ground truth (Eric, 2026-08-20 — authoritative, supersedes the proposal)

**Home is the private BioHub Claude project (moved 2026-10-18).** This section and the facts above are a working copy for site edits. When they change, edit the project first, then sync here.

**Mission.** The BioHub gives companies in Central Massachusetts shared access to the equipment, process development, and trained people to run fermentation at pilot scale — so bioindustrial products invented at the bench can be made here, and bioindustrial companies can start and grow here.

**Vision.** A Central Massachusetts where a bioindustrial company never has to leave to scale.

**Brand lines — each has a defined use. Do not substitute one for another.**

| Line | Defined use |
|---|---|
| Building with Biology | Short form. Headers, signage, merchandise — no claim to defend. |
| The Bioindustrial Revolution starts here. | The podium and banner line. |
| Driving the Bioindustrial Manufacturing Revolution in Central Massachusetts. | The full descriptor. **Website**, letterhead, anywhere the region needs naming. |

The first and third run together as one lockup: **"Building with Biology — Driving the Bioindustrial Manufacturing Revolution in Central Massachusetts."** Note `index.md` already carries exactly this pair as `title:` and `subtitle:`, but the subtitle renders nowhere because the homepage uses `layout: default`.

**Values — INTERNAL ONLY. Do not put these on the public site.** They are written staff-facing ("We are about taking seeds to products", "Work collaboratively, think personally, communicate clearly"), and value 3 describes the target customer in terms that read badly to that customer. Briefly published to `/about/` on 2026-08-20 and removed the same day at Eric's direction. Reproduce **verbatim** wherever they are used internally:
1. **Scale it.** A process that works at the bench is a seed. A process that works at a hundred liters is product. We are about taking seeds to products.
2. **Theory and Practice.** Every project trains someone – a student, a staff, or a partner.
3. **Take the customers the market won't.** A five-person company with a good strain cannot buy time at a contract manufacturer. That is exactly who this is built for.
4. **Be the Hub that connects all the spokes.** We believe our customers, our partners, our staff, our trainees, and our network are all connected. Work collaboratively, think personally, communicate clearly.
5. **Serve Central Massachusetts.** We want things invented here to get made here, by people hired here. Then, if they need to grow beyond the region, we still anchor them here.

Value 5 was revised by Eric on 2026-08-20 — the earlier "It is not enough that something gets invented here" version is superseded. On first install I silently edited values 2 and 4 (tightened "a staff" to "a staff member", compressed the list in 4); both are now verbatim. **Mission, vision, values, brand lines, and the brand story are Eric's text. Copy rules do not apply to them.**

**Brand story** (short form — deck opener, About blurb; not yet on the site):
> The Blackstone Valley is where American industry learned to work — fifty miles of mills from Worcester to Providence, and a city at the head of the river that built the machines everyone else used. WPI was founded there in 1865 on the idea that theory and practice belong in the same building.
>
> Biology is now a manufacturing technology, and the same problem has returned: the science is ready and the infrastructure is not. The BioHub is shared pilot-scale capacity at Gateway Park, so a company with a working process can scale it here.
>
> Same river. Same ethos. New century.

Note value 3 uses "strain" deliberately. The earlier instruction to reduce "strain" sitewide applies to positioning copy, not to this.

**Homepage tracks the mission (2026-08-20).** The old hero — "Between a promising strain and a manufacturable product" plus "screen strains and run pilot-scale fermentations" — led with strain engineering, one of three services, and offered "avoid an offshore CMO queue" as the payoff. The mission promises access to **equipment, process development, and trained people**, with the payoff that products get **made here** and companies **start and grow here**. Hero now opens on the brand line and the lead paraphrases the mission directly. "Strain" went from 9 uses on the homepage to 4, all naming the BioFoundry service; the 11 uses inside `mailto:` intake templates are functional routing fields and stay.

**Homepage cards: three slots, three jobs (2026-08-22).** Each "What we're building" card runs eyebrow → title → body, and no phrase repeats inside a card. Eyebrow carries the **pillar word** (Infrastructure · Innovation · Workforce) in mono caps, so the three eyebrows read across as the same bar that sits above the mission on About. Title carries the **promise** (Scale your process / Build the equipment / Train your team — card 2 retitled 2026-10-18 when it became Builder's Lab only).

**BioFoundry and Pilot Facility merge; Builder's Lab stays separate (Eric, 2026-10-18).** Supersedes the 2026-08-22 three-services rule and the two-link card 2. Screening, strain engineering, and 1–100 L fermentation are one service, **BioHub infrastructure**, described by scale (100 µL–100 L), matching the Oct 2, 2026 one-infrastructure frame in the BioHub folder's CLAUDE.md. The **MBI Builder's Lab** keeps its own section, anchor, and CTA because it is MBI's; never fold it into the infrastructure section. The site must explain clearly what the BioHub can do across scales, not pilot scale alone. Site edits to carry this out are pending Eric's approval (ledger, Open — mine).

Every body ends with a status fragment, parallel across all three, so a reader never takes a planned capability for a running one. Cards carry no links: the placeholder site has no Services page (2026-10-18).

**Leadership block.** Chen's affiliation reads **"Director, WPI Biomanufacturing Education and Training Center (BETC)"** only. WPI's staff directory also lists him as Director of PracticePoint; Eric had that removed 2026-08-20 — naming both centers mixes the org chart. Do not re-add it. Roles are Director · Principal Investigator (Young), Regional Innovation Officer (Weaver), Co-Principal Investigator (Chen) — no "Pilot Facility Lead". No personal email on any name; all contact goes through the shared inbox (Eric, 2026-10-18).

**Naming convention.** Default to **"the BioHub"** throughout. Use **"WPI–MBI BioHub"** in places that need to emphasize the anchor partnership (About hero, About Partners section, partner-facing copy). Don't use "WPI BioHub" alone — that under-credits MBI. Reserve "MassBioHub" for the brand/URL form only.

**Canonical partner URLs.** WPI → `https://www.wpi.edu/`, MBI → `https://mbi.bio/`, MassTech → `https://masstech.org/`. Use these consistently across footer and content pages.

**Hedging principle.** Default voice: **forward-looking, present-state-honest.** "Will feature" not "features." "Designed to support" not "supports." If a page describes an unbuilt capability without hedging, treat it as a bug.

**This repo does not track what exists.** Funding amounts, which governance bodies exist, whether contracts are executed, which spaces are built — none of that belongs in a website repo, because the repo changes when the *site* changes, not when the *facility* does. Verify any capability, funding, or governance claim against the executed charters, or with Eric, **before publishing it**. Do not reconstruct an inventory here.

## Build & Serve

```bash
bundle exec jekyll build --future   # build into _site/
bundle exec jekyll serve --future   # serve with live reload
```

Ruby and the `github-pages` gem (Jekyll 3.10, bundles `jekyll-sitemap`) are the only dependencies. A local build was first run 2026-10-04 and passes clean. `Gemfile.lock` carries both `x64-mingw-ucrt` and `x86_64-linux` so it resolves on Windows and in CI.

## Deployment

GitHub Pages builds and publishes from `main`. The Actions workflow (`.github/workflows/jekyll.yml`) builds with the same `github-pages` gem, so a green check means Pages will build too. Before 2026-10-04 it used `jekyll/builder:latest`, a Jekyll 4 image that did not match production. After a push, hard refresh (`Ctrl+Shift+R`) if the live site looks stale.

## Architecture

**Facts live in one place.** Templates read them; pages never retype them.
- `_config.yml` — `email` (the single inquiry inbox) and `address` (50 Prescott). Used by the inquiry include, the JSON-LD, and `contact.md`.
- `_data/partners.yml` — anchor partners with an `id`. Feeds the Partners cards on `/about/`, the footer logo links (looked up by `id`), and JSON-LD `sameAs`.
- `_data/facts.yml` — every claim that appears on more than one page (MassTech award, NSF wording, partner count, BETC figures, trainee target and year, build-out horizon). Pages read them as `site.data.facts.<key>` or through `{% assign f = site.data.facts %}`.
- `_data/people.yml` — the leadership block on `/about/`.
- `_data/nav.yml` — nav order: **Home · About · Contact**. `cta: true` renders as `.nav-cta`, the outlined pill.

**Layouts.** `page.html` extends `default.html` and adds the page header (`title`, optional `subtitle`). `default.html` holds canonical, OG/Twitter, `Organization` JSON-LD (built with `jsonify`), and the skip link.

**Includes.** `nav.html`, `footer.html`, `partner-card.html`, and `inquiry.html`.

**`inquiry.html` is the only way to write a contact button.** It builds the pre-filled `mailto:` from plain text and encodes it once. Parameters: `label`, `class`, `interest`, `project` (`list` / `optional` / `general`), `omit` (any of `project timeline confidentiality`), `prompt`, `hello="yes"`. The documentation is in the include's header comment. Never hand-encode a `mailto:` again: 13 hand-encoded copies had drifted before 2026-10-04.

Content pages are Markdown with raw HTML blocks. Each sets its own `description:`; the layout falls back to `site.description`. Inside a `<div>`, Markdown needs `markdown="1"`.

## Page map

| Route | File | Purpose |
|---|---|---|
| `/` | `index.md` | **`layout: default`** (no page header, the hero supplies the h1). Hero lockup → CTAs → What we're building (three static cards) → By the numbers (four tiles) → Partner with us (navy band, partnership CTA). Redirect target for `/services/` |
| `/about/` | `about.md` | Brand story → Mission → Vision → Leadership → Partners (cards from `_data/partners.yml`, partnership CTA) → Governance. Redirect target for `/partners/` |
| `/contact/` | `contact.md` | Lead with the inbox address as visible text, one line on who should write, one inquiry button, Gateway Park and Builder's Lab addresses. Redirect target for `/work-with-us/` |

## Design System

**Rule: every colour, type size, and space in `style.css` comes from a token in `:root`.** The only raw values left are geometry: borders of 1–3px, the vessel drawing, logo heights, and grid minimums. A new raw `px`, hex, or `rgba` value outside `:root` is a bug.

### Colors

| Variable | Value | Usage |
|---|---|---|
| `--ground` | `#FAF8F6` | Warm paper page ground |
| `--ground-2` | `#F2EFEC` | Stat band, footer |
| `--surface` | `#FFFFFF` | Cards, lifting off the paper |
| `--fg` | `#23303B` | Body text, headings |
| `--muted` | `#5B6B79` | Secondary text; default mono-label colour |
| `--rule` | `#DFE4E9` | Borders |
| `--navy-900` | `#1E2939` | The partner band on the homepage |
| `--navy-700` | `#323F52` | Links, stat numerals, disclosure summaries |
| `--navy-500` | `#4A586D` | Structural mono labels, vessel outlines |
| `--navy-100` | `#E8ECF3` | Hover wash, vessel liquid |
| `--crimson` | `#AC2B37` | WPI Crimson. Header bar, buttons, eyebrows, stat rules, card tops, person rules, pilot vessel, footer rule |
| `--crimson-dark` | `#8E2030` | Hover |

**On-colour tokens** — type and rules over the crimson header, the mission panel, and the navy band. Do not add ad-hoc alphas: `--on-color` (white) · `--on-color-2` (.85, secondary text, 5.22 on crimson) · `--on-color-rule` (.35, dividers and control borders) · `--on-color-rule-faint` (.18) · `--on-color-wash` (.12, hover) · `--on-color-edge` (black .20, header edge). On the navy band only: `--on-dark` `#EDF3FB` (body), `--on-dark-2` `#A5BBD2` (lead). Before 2026-10-04 there were 11 different white alphas.

**Slate, not navy — the BioMADE problem (2026-08-20).** BioMADE runs the same red-and-blue family: their wordmark samples at `#BC3215` (hue 10, sat 80 — a vermilion) and `#103F68` (hue 208, sat 73 — a saturated navy). The BioHub's blue was `#142743` (hue 216, sat 45), close enough to read as the same scheme in the same sector. Fix was to **desaturate rather than change hue**: same 216, saturation cut to 24. Crimson is now the only saturated colour on the site, which is both the differentiator and better design. WPI Crimson at hue 354 is a wine red against BioMADE's orange-red, and the solid crimson header bar is the single biggest visual separator — BioMADE's header is white with a photo hero. **Do not reintroduce a saturated blue.**

**The crimson rule.** On the paper ground crimson is 6.28 and works as type. Inside `.bleed-dark` it drops to 2.25 and must never carry words there — crimson inside the band is for the button fill only.

**Why navy at 216°.** WPI Crimson sits at 354°. The original teals sat near 200°, close to crimson's complement, and the two vibrated. The navy family is pinned at 215–217° — 139° of separation — which gives the red-white-blue register anchored to WPI Crimson rather than a flag red. WPI Gray `#A9B0B7` is deliberately unused.

**Contrast verified** (AA, lowest passing 4.81): body 13.43 · muted 7.57 · links 8.88 · stat numerals 14.99 · white-on-crimson 6.66. On card surfaces the same tokens read 9.95 / 5.61 / 6.58 / 4.81.

**Header is WPI Crimson.** `.site-header` is `--crimson`, white title, nav links in `--on-color-2`, active underline **white** — a crimson underline on a crimson bar is invisible. The header mark is `biohub_mark_white.png`, a white knockout with no plate (verified in code 2026-10-04; an earlier note here described a white plate holding the full-colour logo). Footer logos are the full-colour originals.

**Logos.** `biohub_logo_transparent.png` keys out the baked-in white of `biohub_logo.png` and is what the JSON-LD points at. `biohub_logo_slate.png` is the homepage hero mark. The unused `wpi_/mbi_/techhub_/biohub_logo_white.png` knockouts were deleted 2026-10-04.

### Type

| Token | Value | Used by |
|---|---|---|
| `--fs-label` | 11px | Mono labels, tags, footer privacy line |
| `--fs-small` | 14px | Buttons, nav, captions, stat notes |
| `--fs-body` | 16px | Body; the mission panel's mono heading |
| `--fs-lead` | 18px | `.lead`, header tagline, mission paragraph, phone site title |
| `--fs-h3` | 22px | h3, site title, mission pillars, phone stat numerals |
| `--fs-h2` | clamp(28,3.4vw,36) | h2 and stat numerals |
| `--fs-h1` | clamp(32,4.4vw,50) | Page titles |
| `--fs-display` | clamp(34,5vw,50) | Homepage hero h1 only |

Letter-spacing: `--track-display` (-.02em) on League Spartan, `--track-label` (.12em) on mono. **Faces** (Google Fonts, `default.html`): League Spartan 500–700 for display, Plus Jakarta Sans 400–700 for body, IBM Plex Mono 400–600 for labels.

**The mono label is defined once.** One grouped rule near the top of `style.css` sets 11px / 500 / .12em / uppercase / `--muted` for `.eyebrow .page-subtitle .stat-l .card-i .split-l .person .role .partner .kind .cgrid b`. Components set only colour and layout. Colour carries the role: **crimson** = identity (eyebrow, role, partner kind), **navy-500** = structure (page subtitle, stat and split labels, contact heads), **muted** = metadata. A new label joins the group; it does not restate the type.

### Space and components

**Spacing scale.** `--s1` 4px through `--s9` 104px. Use these; do not reintroduce ad-hoc padding.

**Buttons.** Every `.button` sits in a `.cta-row`. Contact buttons come from `inquiry.html`.

**Cards.** Every `.card` is a static panel on `--surface` with a crimson top rule; none is a link on the placeholder site. Stats use `.stat`; prose uses `.prose` inside `.split`.

**`.mission`** — crimson panel, white text, centred mono heading, pillars row, left-aligned paragraph. Raw HTML inside.


**Links.** External links open in a new tab with `target="_blank" rel="noreferrer"`. Use the literal `→` character and the straight apostrophe `'`, not `&rarr;` or `&rsquo;`.

### Accessibility
- Skip-to-content link is visually hidden until focused
- `:focus-visible` outlines site-wide; `prefers-reduced-motion` disables transitions
- Header logo has `alt=""` because the wordmark text beside it already names the site
- Cookieless analytics (Goatcounter) — no banner required, but the footer notes the choice

## SEO / metadata
- `<title>`, description, OG, Twitter, and canonical come from page frontmatter in `default.html`
- `Organization` JSON-LD reads name, description, email, and address from `_config.yml` and `sameAs` from `_data/partners.yml`
- `jekyll-sitemap` generates `/sitemap.xml`; `robots.txt` references it
- `site.webmanifest` lives in `assets/img/favicon/`; its icon paths are absolute from the site root
- Internal docs (`CLAUDE.md`, `SITE_PLAN.md`, `LICENSE`, `Gemfile*`) are excluded in `_config.yml`; underscore folders are skipped by Jekyll already

## Adding Content

- **New partner**: add to `_data/partners.yml` with an `id`. It renders on `/about/` and joins JSON-LD `sameAs`
- **New contact button**: `{% include inquiry.html label="… →" interest="…" %}` inside a `.cta-row`
- **New team member**: add an entry to `_data/people.yml`
- **New or changed figure**: if it appears on more than one page, it lives in `_data/facts.yml`
- **New page**: a `.md` file with `layout: page`, `title:`, `description:`, `permalink:`; add to `_data/nav.yml` if it belongs in the nav
