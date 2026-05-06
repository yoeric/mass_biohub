# Site Plan — May 2026

Captured from a planning conversation on 2026-05-05, re-evaluated against the BioHub project folder, then revised after Eric's corrections on naming, contact strategy, and operational reality. This is the working backlog.

## Re-evaluation log (May 2026)

**Round 1 — initial 13 items** captured from looking at the website alone.

**Round 2 — read BioHub project files.** Surfaced the Public Summary outline, the v9 alumni newsletter draft, Action Items decisions, and exec-summary metrics. Added five items (naming, public-paragraph slot, signup, metrics, voice audit). Plan grew to 18.

**Round 3 — Eric's corrections (this round):**

1. **Naming resolved.** Default to **"the BioHub"**. Use **"WPI-MBI BioHub"** in specific places that need to emphasize both anchor institutions (About hero, Network page intro, partner-facing copy). Drop "WPI BioHub" — was wrong to put WPI alone in front of MBI.
2. **One contact point, not three.** Pushback on splitting "Join the Network," "Get in touch," and "Stay in the loop" into separate CTAs — that fragments the experience for a small org. Single CTA model: everything routes to `biohub@wpi.edu` via the pre-filled mailto template, with engagement type as a field in the body. Drops the standalone signup item entirely.
3. **Operational reality.** The BioHub only has **WPI CERES capabilities** today. The Pilot Facility, Builder's Lab, and BioFoundry expansion are all planned but not built — funding arrived only a few months ago and physical space isn't secured. This isn't a hedge problem; the Services page currently describes aspirational infrastructure as if operational, which is a meaningful credibility risk. The hedge item gets upgraded to a structural reframe (item 11 below).
4. **Audience routing — no ChemE-specific card.** A generic "Following along / Interested party" card replaces the ChemE-specific one and serves alumni, curious community, journalists, and partner-curious folks all at once.

**Net change.** Round 3 drops two items (separate signup, standalone Visit page) and restructures one (hedge → reframe). 18 → 16 items.

**Round 4 — Eric's follow-up corrections:**

1. **Hedge harder, everywhere.** Round 3 absorbed the operational-reality fix in items 10 and 11, but didn't carry the principle through the rest of the plan. New "Hedging Principle" callout below applies to every item.
2. **No "stay informed" anywhere except the follow-along card.** Round 3 added "stay informed" as one of the engagement-interest options in the mailto template — that re-fragments the touchpoint. Removed. The follow-along card on Work With Us is the *only* mechanism for low-commitment contacts.
3. **Drop the numerical metrics block entirely.** "500 trainees / 3,000 jobs" are MassTech-report metrics, not visitor-facing. The vision statement already lives on About; no need to duplicate. Item dropped.

**Net change Round 4.** 16 → 15 items.

**Round 5 — Eric's resolutions to outstanding open questions:**

1. Item 11 → **Option B** chosen (restructure Services into Today / Coming online).
2. Item 6 → Public Summary: **lean into Blackstone Valley framing**, **include MassTech attribution** (formal name). $5M figure still TBD.
3. Quinsigamond vs. Quinnebaug Valley CC → **strip the named-school list entirely**. No official partnerships yet, only support letters. Workforce section moves to "regional educators including Worcester-area community colleges and universities."
4. Jon Weaver's MBI title → **add to leadership card**. Folded into item 5 (same About-page edit pass as the naming convention).
5. Network page partner cards → **keep the three anchors** (already the default; confirmed).
6. OG image → only have a white-background logo. Plan now: composite onto a teal canvas at implementation time.

No items added or dropped Round 5 — these are all resolutions inside existing items. Item count holds at 15.

**Round 6 — final two open decisions:**

1. Item 8 follow-along card name → **"Following along."**
2. Item 6 — **omit the $5M figure** from the homepage hero. (Recommend Eric also strip it from the v9 alumni newsletter for consistency.)

All major design decisions now resolved. The plan is ready to execute pending the user-provided inputs listed in Open Questions (CERES capabilities, MBI description, GoatCounter snippet, Public Summary draft completion).

**Round 7 — implementation pass (2026-05-06):**

Items 1–5, 7–9, 11–12, 14–15 implemented in a single session. Specific changes:

1. **Nav slimmed** — `_data/nav.yml` trimmed to Home · Services · Work With Us · Network · About. News and Contact removed from nav.
2. **Partners → Network** — `partners.md` title updated; permalink `/partners/` preserved for SEO.
3. **MBI partner entry fixed** — URL corrected to `https://mbi.bio/`; description rewritten to reflect bioindustrial mission (not clinical trials).
4. **Homepage cards realigned** — "What we do" → "What we're building"; cards renamed Network / Projects / Workforce Development with deep links to `/services/` anchors and hedged blurbs.
7. **"Mission" CTA renamed** — now reads "Learn about us". Third CTA updated from "Partner with us" → "Work with us" linking to `/work-with-us/`.
5. **Leadership card fixed** — Jon Weaver now shows "Regional Innovation Officer, WPI-MBI BioHub" and "President & CEO, Massachusetts Biomedical Initiatives" on two separate muted lines.
   **About page polish** — "Where we sit" reframed to anchor on CERES and hedge pilot infrastructure. "Lead Partner Websites" section removed (moved to footer). Subtitle added.
8. **Work With Us restructured** — five audience sections: Startup founder · Industry partner · Researcher/educator · Job seeker/trainee · Following along. Each section has a pre-filled `mailto:` CTA customized to that audience.
9. **Contact page replaced** — nested bullet list removed; now a single pre-filled `mailto:` button with URL-encoded subject and body template.
10+11. **Services page reframed (Option B)** — lead paragraph hedged; "Project Resources" block replaced with "Available today" (CERES anchor) and "Coming online over the next three years" sections. Each planned resource wrapped in a `<details>` block labeled "Planned equipment & specs." Workforce section: named schools (Quinsigamond, WPS, UMass, Tufts) replaced with generic "regional educators including Worcester-area community colleges and universities."
12. **Footer updated** — "Funded by the Massachusetts Technology Collaborative." credit added. Resources links row added: News · Contact · Regional Biomanufacturing Strategy PDF. "Lead Partner Websites" removed from `about.md`.
   **CSS additions** — `<details>`/`<summary>` styling, `.footer-credit`, `.footer-links`.
14. **Voice audit** — clean. No "cutting-edge" or "state-of-the-art" found in content pages. "Ecosystem" hits all anchored to "bioindustrial ecosystem" (kept per plan). "Next generation" hits specific (biomanufacturing talent) — kept.
15. **Polish** — OG/Twitter meta tags added to `_layouts/default.html` (og:type, og:url, og:title, og:description, og:image, twitter:card, twitter:title, twitter:description, twitter:image). All six public pages now have subtitles.

6. **Homepage lead paragraph replaced** — Eric provided the finalized Variant B layman paragraph on 2026-05-06. Installed in `index.md`. Leads with "The BioHub" (bolded), Blackstone Valley framing, MassTech attribution, no $5M figure. Item complete.

13. **GoatCounter added** — script tag installed in `_layouts/default.html` before `</body>`. Account: `biohub.goatcounter.com`. Item complete.

**Still open:**

- OG image: currently using white-background `biohub_logo.png`. Better path (teal canvas composite onto `--header-bg` #2A6F8A at 1200×630) is documented but not yet executed.

## Hedging Principle (applies to every item)

The BioHub has $5M in funding (received Q1 2026), a Governing Board, the BioLector hardware (in commissioning), and the WPI CERES capabilities that pre-date this initiative. **It does not yet have:** the Pilot Facility, the Builder's Lab, the BioFoundry expansion, dedicated physical space beyond CERES, an Executive Director, a Technician, a Marketing & BD Manager, executed member contracts, or operational pilot fermentation.

Default voice across the site: forward-looking, present-state-honest. "Will feature" not "features." "Coming online over the next three years" not "operational." "Designed to support" not "supports." Match the v9 alumni newsletter's tone. If this plan ever describes a capability without hedging, treat it as a bug.

## Implementation order

1. Hide News from the homepage and top nav
2. Slim navigation to 5 items and fold Contact into Work With Us / Network
3. Fix the MBI partner entry (URL + description)
4. Realign homepage "What we do" cards to match the Services pillars (and hedge the blurbs)
5. Apply naming convention site-wide ("the BioHub" default, "WPI-MBI BioHub" in institutional contexts)
6. Replace homepage lead paragraph with the finalized public layman paragraph
7. Rename the homepage "Mission" CTA to "Learn about us"
8. Add audience routing to Work With Us — five cards, last one is a generic "Following along" entry (the only low-commitment touchpoint on the site)
9. Replace the Contact page bullet list with a pre-filled `mailto:` template (single CTA across the site)
10. Wrap equipment specs in expandable details, clearly labeled "planned" where the resource isn't built yet
11. **Reframe Services page (and adjacent copy) to current state vs. planned state** — the big one
12. Build a footer with partner logos, Massachusetts Technology Collaborative credit, and the Strategy PDF link
13. Add GoatCounter analytics
14. Voice/phrase audit (cut "cutting-edge / state-of-the-art / ecosystem" boilerplate)
15. Polish: standardize subtitles, audit OG image / favicon, run contrast check

**Deferred / dropped:**

- ~~Visit page~~ — deferred until the BioHub has its own physical presence beyond CERES. "Where we sit" on About is enough for now.
- ~~Stay-in-the-loop signup~~ — dropped per the single-CTA principle.
- ~~Numerical metrics block (500 trainees / 3,000 jobs / etc.)~~ — dropped per Round 4. Internal MassTech-report metrics, not visitor-facing. About already has a vision statement.

---

## 1. Hide News

**Decision.** Remove the "Latest news" `hero-card` from `index.md`. Drop the News entry from `_data/nav.yml`. Keep `news.md` reachable via a footer link.

**Why.** `_data/news.yml` has one entry from Feb 2026. An empty news feed in a homepage hero card actively undercuts credibility.

**Files.** `index.md`, `_data/nav.yml`, `_includes/footer.html`.

## 2. Slim navigation

**Decision.** Final nav: **Home · Services · Work With Us · Network · About**.

- Rename `Partners` → `Network`.
- Drop `Contact` from the nav. The mailto template (item 9) becomes the conversion CTA on Work With Us and Network, both pointing to `biohub@wpi.edu`.
- Drop `News`.

**Files.** `_data/nav.yml`, `partners.md` (rename and update title), `contact.md` (keep file or delete; if kept, link from footer only), `work-with-us.md`, Network page.

**Open question.** Keep `permalink: /partners/` after renaming the page (recommended — preserves inbound links and SEO) or change to `/network/` and add a redirect.

## 3. Fix MBI partner entry

**Decision.** In `_data/partners.yml`:

- Change URL from `https://www.mass.gov/orgs/massachusetts-bioindustrial-initiative` to `https://mbi.bio/`.
- Pull description directly from `mbi.bio` and trim to ~25 words.

**Why.** The current description is for a different MBI program (clinical trials). CLAUDE.md confirms `https://mbi.bio/` as canonical.

**Files.** `_data/partners.yml`.

## 4. Realign homepage "What we do" cards

**Decision.** Rename the three homepage cards from "De-risk scale-up / Enable builders / Accelerate innovation" to **Network / Projects / Workforce Development** to match the Services page pillars. Deep-link each to the matching anchor (`/services/#network`, `/services/#projects`, `/services/#workforce`). Rewrite each blurb in 1–2 sentences.

**Hedging note.** Per the Hedging Principle, blurbs must reflect "we're building" rather than "we have." E.g., Network → "Connecting industry, academic, and public-sector partners across the bioindustrial community we're building in Central Massachusetts." Projects → "Sponsored and collaborative R&D in process development, scale-up, and strain engineering — coming online over the next three years." Workforce Development → "Hands-on training and certificate pathways for the next generation of biomanufacturing talent, in development with regional educators." (Working drafts — refine on implementation.)

Consider also retitling the section heading from "What we do" → "What we're building" to set tense honestly at the top.

**Files.** `index.md`.

## 5. Naming convention + leadership card

**Decision (resolved).** Default to **"the BioHub"** throughout. Use **"WPI-MBI BioHub"** specifically when emphasizing the anchor partnership — likely places: About hero, Network page intro, the Partners block. Use **"MassBioHub"** only as the brand/URL form. Drop "WPI BioHub" wherever it currently appears (CLAUDE.md uses it but that's internal — public-facing should reflect the joint anchor).

**Bundled in same About-page edit pass: Jon Weaver leadership card.** Add his MBI title (Round 5 decision). Per CLAUDE.md, the full title is "Regional Innovation Officer, WPI-MBI BioHub; CEO, Massachusetts Biomedical Initiatives." On the leadership card, render as two `<p class="muted">` lines:

```html
<p class="muted">Regional Innovation Officer, WPI-MBI BioHub</p>
<p class="muted">President & CEO, Massachusetts Biomedical Initiatives</p>
```

**Files.** All `.md` page files; site title in `_config.yml`; header alt text in `_layouts/default.html`; `about.md` leadership card for Jon Weaver.

**Action item.** Single grep + edit pass. Note: the v9 alumni newsletter currently uses "WPI BioHub" — flag for Eric to update on the newsletter side (or leave if it's already in print).

## 6. Replace homepage lead paragraph

**Decision.** Replace the current `index.md` lead paragraph with the Variant B layman paragraph being produced in `Public_Summary/`.

**Files.** `index.md`.

**Blocked on.** Public Summary draft completion. All open questions in that outline are now resolved:

- Name to lead with — resolved by item 5 ("the BioHub" / "WPI-MBI BioHub").
- Lean into Blackstone Valley framing — **yes** (matches v9 alumni newsletter).
- MassTech attribution language — **include**, formal name "Massachusetts Technology Collaborative."
- Whether to include the $5M figure — **omit** (Round 6). The site stays focused on the mission and partnership, not the funding level. Note: the v9 alumni newsletter does include "$5M" — flag for Eric whether the newsletter copy should be updated for consistency.

**Reference voice.** The v9 alumni newsletter is the canonical model for tone, hedging, partner attribution, and Blackstone Valley framing — minus the $5M reference.

## 7. Rename "Mission" CTA

**Decision.** In `index.md`, the CTA row reads "Mission · Explore services · Partner with us." Rename "Mission" → "Learn about us." Destination stays `/about/`.

**Files.** `index.md`.

## 8. Audience routing on Work With Us

**Decision.** Restructure `work-with-us.md` so each audience has its own labeled, deep-linkable section. Five audiences:

- **Startup founder** — fast facility access, no equity, contract services
- **Industry partner** — research partnerships, multi-year agreements, IP framework
- **Researcher / educator** — curriculum collaboration, joint R&D, faculty access
- **Job seeker / trainee** — workforce development tracks, certificate pathways
- **Following along** — for anyone who wants to keep tabs but isn't ready to engage formally: alumni, curious community members, journalists, partner-curious folks. Short — one or two sentences plus the same `biohub@wpi.edu` CTA. **This card is the only mechanism on the entire site for low-commitment contacts** — there is no separate signup form, no "stay informed" option in the mailto template, no newsletter list. Anyone who emails through this card and asks to keep tabs gets manually added to whatever update mechanism the BioHub team chooses.

Every section ends with the same CTA pointing to the mailto template (item 9). The five audiences are differentiated by *what they say in the email body*, not by separate forms or addresses.

**Files.** `work-with-us.md`.

**Naming — resolved (Round 6).** **Following along.** Card heading reads "Following along" — friendly, matches a "watcher" role without implying a subscription mechanism.

## 9. Replace Contact bullet list with mailto template

**Decision.** Replace the six-level nested bullet list with a single pre-filled `mailto:` button. URL-encode subject and body so the mail client opens with a populated form. This is the **single contact point** for the entire site — every audience CTA, every "join the network" link, every "get in touch" routes here.

```
Subject: BioHub inquiry — [your organization]
Body:
Organization:
Point of contact:
Engagement interest (network / facilities / curriculum / hiring trainees):
Project type (if applicable — scale-up / prototyping / process development / strain engineering):
Timeline:
Confidentiality constraints:

Tell us about your project (or just say hi):
```

**Important.** The engagement-interest list does **not** include "stay informed" or "follow along." Those visitors arrive via the follow-along card on Work With Us (item 8), which uses the same mailto button but a slightly different default message — that's the entire mechanism for low-commitment contacts. Splitting "stay informed" into the engagement-interest list would re-fragment the touchpoint.

**Files.** `contact.md` (or wherever Contact CTAs live after item 2).

## 10. Expandable equipment specs (with planned labels)

**Decision.** On the Services page, wrap equipment details in `<details>` blocks under each resource card. Critical addition given the operational reality: any spec list for a not-yet-built resource is labeled **"Planned equipment"** (not "Equipment & specs"). This pairs with item 11.

```html
<details>
  <summary>Planned equipment &amp; specs</summary>
  <ul>
    <li>Beckman Coulter BioLector microbioreactor (received Q1 2026, commissioning underway)</li>
    <li>Two Sartorius Ambr250 systems (planned)</li>
    <li>Liquid-handling automation for parallel DBTL cycles (planned)</li>
  </ul>
</details>
```

**Files.** `facilities.md`, `assets/css/style.css` (for `<summary>` styling).

## 11. Reframe Services page to current vs. planned state — THE BIG ONE

**Decision.** This is the largest single change in the plan. The current Services page describes the BioFoundry, Scale-Up Lab, and Builder's Lab as operational facilities. They aren't. Per Eric: **only WPI CERES is operational today**, and even the BioLector that lives there is in commissioning. The other facilities don't have physical space yet.

**Two structural options. Decide before implementation.**

- **Option A — Status badges per resource.** Keep the three resource cards on the Services page, but add a status pill to each: "Operational" (CERES today), "In commissioning" (BioLector), "In build-out" (Builder's Lab electrical upgrade), "Planned" (Pilot Facility, full BioFoundry expansion). Lightest touch but visitors still scan three cards as if they were three live resources.
- **Option B — Restructure into "Today" and "Coming online."** Replace the three-card Project Resources block with two clearly-separated sections: a "What's available today" section anchored on CERES, and a "What's coming online over the next three years" section that lays out the planned Pilot Facility / Builder's Lab / BioFoundry expansion with target dates from the Q1 report (Pilot Facility construction Q2 2026, Builder's Lab Q3 2026, BioFoundry equipment Q2 2026, first scale-up projects Q3 2026). Much more honest and matches the v9 alumni newsletter's "coming online over the next three years" framing.

**Resolved: Option B** (Eric, Round 5). Restructure the Services page into a "What's available today" section anchored on CERES + a "Coming online over the next three years" section with the Pilot Facility / Builder's Lab / BioFoundry expansion and target dates from the Q1 report. Match the v9 alumni newsletter framing.

**Adjacent copy that needs the same treatment:**

- `about.md` "Where we sit" section currently says "The BioHub is anchored at WPI Gateway Park…" — confirm the anchor is just the CERES space today, not a dedicated BioHub facility, and rephrase if needed.
- `work-with-us.md` says "Use BioHub equipment and pilot infrastructure on a fee-for-service basis — hourly or by project." With most equipment not yet operational, this is misleading. Rephrase to "Today: connect with us about CERES capabilities and join the network. Soon: pilot fermentation, Builder's Lab access, full DBTL workflows."
- Homepage cards (item 4) — the Projects card blurb should reflect that projects are in early intake, not full production.
- **Workforce section** (also on `facilities.md`) currently names Quinsigamond Community College, Worcester Public Schools, UMass Amherst, and Tufts as partners. Per Eric (Round 5): no official partnerships yet, only support letters — strip the named list and replace with generic framing like "regional educators including Worcester-area community colleges and universities." This also resolves the Quinsigamond vs. Quinnebaug Valley naming ambiguity by sidestepping it.

**Files.** `facilities.md`, `about.md`, `work-with-us.md`, `index.md`.

## 12. Footer with partner logos

**Decision.** Build out `_includes/footer.html`:

- **Lead partners** — logos for WPI, MBI, MassTech, each linking to the partner's site. Use the existing files in `assets/img/logos/`.
- **Funding credit** — *Funded by the Massachusetts Technology Collaborative.* Use the formal name (not "MassTech Collaborative"). Place above or beside the logos.
- **Resources / page links** — Regional Biomanufacturing Strategy PDF, News, Contact (since they're not in the top nav). No signup link (per the single-CTA principle).

Remove the "Lead Partner Websites" section from the bottom of `about.md`.

**Files.** `_includes/footer.html`, `about.md`, `assets/css/style.css`.

## 13. GoatCounter analytics

**Decision.** Add GoatCounter's tracking script to `_layouts/default.html`. Free for non-commercial, no cookies, no consent banner.

**Files.** `_layouts/default.html`.

**Blocked on.** User signs up at `https://www.goatcounter.com/signup` and sends the script tag.

## 14. Voice/phrase audit

**Decision.** The Public Summary tone spec bans phrases that "signal press release and cause readers to skim": **"innovation ecosystem," "cutting-edge," "state-of-the-art."** Spot-check the live site and replace with concrete, specific language.

Likely candidates (audit-pending):

- "state-of-the-art" — find/cut
- "ecosystem" — keep where it's anchored to a real noun ("regional bioindustrial ecosystem"); cut where vague
- "cutting-edge" — find/cut
- "next-generation" — keep if specific, cut if filler
- "thriving" — soft enough to keep

**Files.** All `.md` page files. Single grep + edit pass.

## 15. Polish

**Standardize subtitles.** Today: Services and Partners have `· `-separated subtitles; About and Contact don't. Add to `about.md` and `contact.md`.

**OG image + favicon audit.** In `_layouts/default.html`, confirm `<link rel="icon">`, `<meta property="og:image">`, `<meta property="og:title">`, `<meta property="og:description">`, `<meta name="twitter:card">`. Add what's missing.

**OG image — current asset is white-background only** (Round 5). Two choices:

- **Quick path:** use the existing white-background BioHub logo as the OG image at `assets/img/og-default.png`. Works, but looks plain in link previews against Slack/LinkedIn's own backgrounds.
- **Better path:** I composite the existing white-background logo onto a 1200×630 teal canvas (`--header-bg` #2A6F8A) programmatically with ImageMagick or similar. Single command, takes a minute, no new artwork needed. Ships a real branded OG image.

Recommendation: better path. Saved to `assets/img/og-default.png`.

**Contrast check.** `--muted` (#527A8A) on `--bg2` (#EAF2F5) is borderline for WCAG AA. Test via WebAIM; if it fails, darken to ~`#3F6878`.

**Files.** `_layouts/default.html`, `assets/css/style.css`, `about.md`, `contact.md`.

---

## Open questions

**Resolved Round 5:**

- ~~Item 11 — Option A or B?~~ → **Option B** (restructure into Today / Coming online).
- ~~Public Summary: lean into Blackstone Valley?~~ → **Yes.**
- ~~Public Summary: required MassTech attribution language?~~ → **Yes**, formal name "Massachusetts Technology Collaborative."
- ~~Quinsigamond vs. Quinnebaug Valley CC?~~ → **Neither.** Strip the named school list from the Workforce section per item 11; no official partnerships yet.
- ~~Add Jon Weaver's MBI title to the About leadership card?~~ → **Yes**, two muted lines: "Regional Innovation Officer, WPI-MBI BioHub" and "President & CEO, Massachusetts Biomedical Initiatives." Folded into item 5.
- ~~OG image asset?~~ → Use the existing white-background BioHub logo, composited onto a teal canvas at implementation time.
- ~~Network page partner cards~~ → keep WPI/MBI/MassTech as the only anchor partner cards.

**Still open:**

- **Permalink** for the renamed Network page — keep `/partners/` (recommended — preserves inbound links) or change to `/network/` and add a redirect? Low-stakes; can be decided at implementation time.

**Content/infrastructure to provide:**

- Which capabilities at WPI CERES are operational today (so item 11's "What's available today" section is accurate)? At minimum: BioLector status — received Q1 2026, commissioning when? Anything else at CERES that the BioHub can offer today?
- MBI description copy — pull from mbi.bio at implementation time.
- GoatCounter script tag — user signs up and sends the snippet.

**Recommended action outside the website:**

- Update the v9 alumni newsletter copy: change "Visit massbiohub.org to learn more and sign up" → "Visit massbiohub.org to learn more and get in touch" so it matches the site's single-CTA model. Or leave the newsletter alone if it's already gone to print and instead ensure the site's contact CTA is unmissable to a visitor following the newsletter link.

## Things explicitly decided NOT to do

- Add additional partners to the Network page beyond the three anchors.
- Add facility/equipment photography (infrastructure still being built).
- Add a Careers page (no openings to list yet, even though three roles are coming per the Action Items doc).
- Add audience-routing cards on the homepage (kept on Work With Us instead).
- Use Plausible or GA4 for analytics (chose GoatCounter).
- Surface DoD / SHIELD content on the public site.
- Surface tier names, fees, contract templates, or the Codomax / Holobiome / Literally Cotton company references on the public site.
- Add a separate newsletter signup form (per the single-CTA principle).
- Build a standalone Visit page (deferred until the BioHub has dedicated physical space beyond CERES).
- Single out WPI ChemE alumni as their own audience-routing card (replaced with the generic "Following along" card).
- Add a numerical metrics block (500 trainees / 3,000 jobs / etc.) — those are MassTech-report metrics, not visitor-facing aspirations. The vision statement on About is the visitor-facing version and doesn't need duplicating.
- Add "stay informed" as an option in the mailto template's engagement-interest list — would re-fragment the touchpoint that the follow-along card already owns.
