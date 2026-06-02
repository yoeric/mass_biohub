# BioHub Website Audit

Date: 2026-06-02. Audited against `BioHub_exec_summary.docx`, `BioHub_final_proposal.docx`, `WPI_Bioindustrial_SOI_final.pdf`, and the user-provided positioning summary. Findings are ranked by impact. Each item has a proposed fix; nothing has been changed yet.

---

## P0 — Factual errors to fix immediately

These are wrong in ways a partner, journalist, or grant officer would catch.

### 1. CERES is misnamed on `/services/`
- **Where:** `facilities.md` line 56 — "WPI CERES (Center for Excellence in Biomedical Research and Science)"
- **Truth:** Across the exec summary, final proposal, and SOI, CERES = **Cell Engineering Research Equipment Suite**. CLAUDE.md also notes this in the image-folder description.
- **Fix:** Replace with "WPI CERES (Cell Engineering Research Equipment Suite)".

### 2. BETC is misnamed on `/about/`
- **Where:** `about.md` line 64 — "Director, WPI Biomedical Engineering & Biotechnology Center (BETC)"
- **Truth:** BETC = **Biomanufacturing Education and Training Center** (proposal §B.2; also referenced throughout). The site name is wrong and slightly comical (it doesn't match the acronym).
- **Fix:** "Director, WPI Biomanufacturing Education and Training Center (BETC)".

### 3. Jon Weaver's MBI title is wrong in the governance block
- **Where:** `about.md` line 75 — "MBI Executive Director"
- **Truth:** Proposal repeatedly identifies him as **President & CEO of MBI** (and the leadership card immediately above gets it right).
- **Fix:** Change "MBI Executive Director" → "MBI President & CEO" — or, better, replace the governance structure entirely (see #4).

### 4. Governance structure on `/about/` doesn't match the funded proposal
- **Where:** `about.md` lines 70–79
- **Site says:** Governing Board chaired by WPI VP for Research, with MBI Executive Director, MassTech rep, and two rotating industry reps.
- **Proposal says (§Governance):** Leadership Council = PI Young, Co-PI Chen, RIO Weaver, MassTech designee (if desired), Tier 1 members, and one rotating external stakeholder — supported by a broader Advisory Board.
- **Fix:** Rewrite to mirror the proposal. A wrong governance structure on a funded-program page is a credibility problem if anyone from MassTech sees it.

### 5. Eric Young's rank is likely stale
- **Where:** `about.md` line 53 — "Associate Professor"
- **Truth:** SOI shows "Assistant Professor" (older doc, so promotion is plausible). The proposal omits the rank.
- **Fix:** Confirm current title with Eric and update if needed. Low-stakes but worth a five-second check.

### 6. Pilot scale floor: 1L vs 2L mismatch across your own sources
- **Where:** `facilities.md` line 84 — "Bioreactors from 2L through 150L (planned)"
- **Sources:** Your chat summary and the **exec summary** say **1L–150L**. The **final proposal** says **2L–150L**.
- **Fix:** Decide once and use it everywhere — exec summary, website, deck. The lower number is more impressive if it's accurate.

### 7. Leadership card omits the Co-PI's role on the Pilot Facility
- **Where:** `about.md` Dr. Liaohai Chen card
- **Gap:** Proposal positions Chen as Director of BETC **and** the Co-PI leading Project 1 (the Pilot Facility). The site shows only the BETC title.
- **Fix:** Add "Co-PI, BioHub Pilot Facility" or similar — it explains why a BETC director is in the BioHub leadership card.

---

## P1 — Positioning: your best line is missing from the site

Your one-paragraph summary to me was sharper than anything currently on the site. The site buries the value proposition; your summary leads with it.

### 8. The "without queuing at an offshore CMO or building it themselves" framing is nowhere on the site
- **Where it should go:** `index.md` lead paragraph
- **Why it matters:** That's the customer-facing pain. Everything else (Network/Projects/Workforce) is an internal taxonomy. A founder reading the homepage should immediately recognize their problem.
- **Proposed lead:**
  > **The BioHub** is a shared bioindustrial manufacturing facility at Gateway Park in Worcester, built so early-stage companies can run pilot-scale fermentations, engineer microbial hosts, and develop new bioprocesses under one roof — without queuing for slots at an offshore CMO or building the infrastructure themselves. Led by WPI and Massachusetts Biomedical Initiatives and funded by the Massachusetts Technology Collaborative, the BioHub exists to compress the time, cost, and risk between a promising strain and a manufacturable product.

### 9. The mission statement on `/about/` is weaker than the one in the proposal
- **Site:** "Enable rapid development and translation of bioindustrial technologies through shared infrastructure, expertise, and partnerships."
- **Proposal:** "Power the bioindustrial revolution in Central Massachusetts, advancing the Ecosystem Readiness Level to 6 in three years."
- **Fix:** Use the proposal mission, or a hybrid. The proposal version is specific, ambitious, time-bound, and has a measurable goal.

### 10. "The Moment" is missing entirely
- **Gap:** Exec summary opens with: Biomanufacturing is one of six U.S. Critical Technology Areas; McKinsey sizes the global opportunity at $200–300B over 10–20 years. None of that urgency appears on the site.
- **Fix:** Add a short "Why now" block to `/about/` or as a homepage section under the lead. Three sentences is enough — credibility comes from the citation, not length.

### 11. Three pillars are too abstract
- **Where:** Homepage and Services use "Network · Projects · Workforce Development."
- **Issue:** "Projects" is a category, not a service. A founder skimming doesn't know if "Projects" means *they can run one* or *we run them internally*.
- **Fix:** Either rename to outcomes-oriented terms ("Scale your process · Engineer your strain · Train your team") or push the **Pilot Facility · BioFoundry · Builder's Lab** trio to the front, since those are the named, fundable, real things.

### 12. Headline numbers from the proposal aren't on the site
- **Missing:** $5M+ MassTech investment · 35 supporting partners · 500 trainees over 3 years · 90% job placement target · target 3,000+ jobs · 20X ROI · 33 letters of support.
- **Fix:** Add a "By the numbers" strip on `/about/` or homepage. These are the credibility signals that make a new visitor take the project seriously.

### 13. BETC's existing track record isn't leveraged anywhere
- **Gap:** BETC has trained 3,000+ people over 11 years. The site never says this. It's one of the strongest "we know how to operate" signals you have.
- **Fix:** Add to `/about/` "Where we sit" section, e.g.: "We build on top of BETC, which has trained over 3,000 biomanufacturing professionals since 2013."

### 14. "Available today" understates what's actually available
- **Where:** `facilities.md` "Available today" — currently only lists a BioLector (which itself is "commissioning underway") and "WPI faculty expertise."
- **Reality:** CERES is an established research equipment suite with a multi-year user base of WPI faculty and ~10 partner companies (per SOI). That's the real "available today."
- **Fix:** Reframe CERES as a real operating facility, list its actual current capabilities, and clearly distinguish what's coming (Ambr250s, microbioreactor expansion, pilot facility, Builder's Lab).

---

## P2 — Content gaps

### 15. Partners page only lists 3 entries — but the messaging is "35 partners"
- **Where:** `_data/partners.yml`
- **Issue:** Proposal mentions 35 stakeholder letters, including 17 bioindustrial-specific companies (Holobiome, Codomax, Galy, Ark Biotech, Sartorius, Beckman Coulter, ThermoFisher, ProAnalytics, Sunflower Tx, EvoBioWorks, BASF, Ginkgo, Coghlin, Festo, etc.). The site shows only WPI, MBI, MassTech.
- **Fix:** Decide which partners are public-OK to list, group them (Anchor institutions · Industry · Equipment · Workforce/Education · Government), and add them. A network page that shows three logos contradicts the "Network" claim. If permissions are still being collected, at minimum add the named anchor projects (Holobiome, Codomax, Galy as first pilot projects) and equipment partners (Sartorius, Beckman Coulter, ThermoFisher, ProAnalytics) — those are in your public proposal.

### 16. News page has one entry from February
- **Where:** `_data/news.yml`
- **Issue:** Today is June 2026. The site claims the BioHub "launched in 2026" yet news shows nothing since launch. Stale-news pages signal "this organization isn't active."
- **Fix:** Either backfill 3–5 items (NSF Biofoundries award, Beckman Coulter BioLector commissioned, MassTech funding announcement, BioHub Day kickoff, etc.) or remove the page from nav until it's populated. Also: News isn't in the nav (only footer), so it's currently a ghost page either way.

### 17. Latest News card is missing from the homepage even though CLAUDE.md specifies it
- **Where:** `index.md` vs CLAUDE.md "Page Notes" for index.md
- **Issue:** CLAUDE.md says homepage ends with a "Latest News (hero-card)." The current `index.md` has no news block at all.
- **Fix:** Either add the news block (the include exists) or update CLAUDE.md to reflect the actual design.

### 18. First pilot projects (Holobiome, Codomax, Galy) deserve a featured spot
- **Where:** Currently absent
- **Why:** Proposal names these as the first three pilot projects launching Q3 Year 2. Each is a clean, concrete story (gut microbiome, low-cal sweetener, lab-grown cotton). Together they show the BioHub already has anchor customers — which is the single hardest thing to communicate for a new facility.
- **Fix:** Add a "Founding pilot projects" section on `/services/` or homepage. Cards with a one-line description and a link out.

### 19. AI and AR/VR — the differentiators — barely show up
- **Gap:** The proposal frames AI integration (real-time process modeling, digital twins, OPC-UA data pipelines) and AR/VR training as the two emerging technology areas that make the BioHub distinctive. The site mentions "automated DBTL workflows with AI" once and "Digital-twin and AR/VR-enabled instruction" once.
- **Fix:** Either give each its own section/card on `/services/`, or make a "How we're different" block. As-is, the site reads like every other shared facility.

### 20. No address, hours, location map, or photo of the actual place
- **Where:** `contact.md` and `index.md`
- **Issue:** "Gateway Park in Worcester" is mentioned but never with a street address or map. Building credibility for a physical facility without showing the physical facility is hard.
- **Fix:** Add 60 Prescott St / Gateway Park address + an embedded map or static photo. The MBI Builder's Lab is at 17 Briden St per the proposal — name it too.

### 21. Tiered Membership / Fee-for-Use Model is not surfaced
- **Where:** Currently absent (proposal §Sustainability Plan describes Tier 1: $150k/yr, Tier 2: $75k/yr, Tier 3: $25k/yr)
- **Issue:** A partner ready to sign up has no on-ramp shown on the site. The "Industry partner" section of `/work-with-us/` is generic.
- **Fix:** Decide whether the membership tiers are public yet; if yes, add a "Become a member" page with the tier structure. If still in flux, add a "Membership options coming soon — get in touch" line.

### 22. The Regional Biomanufacturing Strategy is footer-only
- **Where:** Footer link to the strategy PDF
- **Issue:** That document is the intellectual foundation for the whole BioHub thesis (proposal cites it as ref 1). On the site it's a footer afterthought.
- **Fix:** Reference it inline in `/about/` ("Where we sit") as the blueprint that identified the three gaps the BioHub fills.

### 23. No mention of the $5M+ investment, NSF Biofoundries award, or other federal/state credentials
- **Where:** Absent
- **Issue:** "WPI is one of the five NSF-funded Biofoundries with potential for $24M after planning phase." That's a major credibility signal and it's not on the site.
- **Fix:** Add a short "Funded by / supported by" line to `/about/` with named programs and amounts you're willing to publish.

---

## P3 — UX and information architecture

### 24. News is in the footer but not in the nav
- **Where:** `_data/nav.yml`
- **Issue:** News exists as a page but only the footer links to it. CLAUDE.md actually documents News as part of the nav order, so the nav is also out of sync with the docs.
- **Fix:** Either add News to nav (and populate it — see #16) or remove the page.

### 25. Homepage cards link to `/services/#anchor` — but `/services/` also has the same cards linking to the same anchors on itself
- **Where:** `index.md` cards → `/services/#network` etc. On `/services/`, the same three cards link to `#network` (i.e., themselves).
- **Issue:** Two-hop navigation that goes nowhere new. The Services page also leads with the same 3 cards as the homepage, so a visitor sees the same content twice in a row.
- **Fix:** Either drop the cards from one of the two pages, or make `/services/` link out to dedicated `/pilot/`, `/biofoundry/`, `/builders-lab/` pages (which is probably the right answer once those are real).

### 26. Contact page is one button and one sentence
- **Where:** `contact.md`
- **Issue:** Anyone landing here directly has nothing to read. No phone, address, social, or alternate contacts. No "what to expect after you email."
- **Fix:** Add address, response time expectation, alternate contacts (Jon Weaver at MBI, biohub@wpi.edu, social/LinkedIn if any), and a short FAQ. Currently this page makes the org feel small.

### 27. Homepage has no image
- **Where:** `index.md`
- **Issue:** First impression is a wall of text. A hero photo of Gateway Park, the BETC, or a fermenter would massively change the read.
- **Fix:** Add a hero image. The CTA row would benefit from sitting under a visual.

### 28. CTA buttons are all navigational, none is conversion-oriented
- **Where:** `index.md` cta-row
- **Issue:** "Learn about us · Explore services · Work with us" — three "go look at another page" buttons. None says "Email us" or "Become a member."
- **Fix:** Replace one with a direct contact CTA or a "Schedule a tour / intro call" link.

### 29. "Work With Us" personas are great but invisible from the homepage
- **Where:** `/work-with-us/` has well-written persona-based entry points; homepage doesn't surface them.
- **Fix:** Surface the four personas (Startup founder · Industry partner · Researcher/educator · Job seeker) as a homepage section with deep links into the right anchors.

### 30. "Network" label vs. "Partners" content
- **Where:** Nav label is "Network", page title is "Network", but content is a list of partners, and the URL is `/partners/`.
- **Issue:** Mild semantic mismatch. "Network" implies more (events, members, calendar, BioHub Day). Currently it's just partner cards.
- **Fix:** Either flesh it out (add the BioHub Network / Leadership Council / Advisory Board / BioHub Day described in the proposal §4), or rename it back to "Partners."

---

## P4 — SEO, metadata, accessibility, polish

### 31. Pages don't define their own `description` frontmatter
- **Where:** All `.md` pages
- **Issue:** Every page falls back to the site-level description, which makes SERPs and social cards generic.
- **Fix:** Add a unique `description:` to each page's frontmatter (~140 chars).

### 32. No structured data (JSON-LD)
- **Where:** `_layouts/default.html`
- **Fix:** Add an `Organization` JSON-LD block with `name`, `url`, `logo`, `sameAs` (WPI, MBI, MassTech URLs), and `parentOrganization` if appropriate. Helps search engines and rich results.

### 33. No canonical link
- **Fix:** Add `<link rel="canonical" href="{{ page.url | absolute_url }}" />` in `default.html` head.

### 34. No sitemap.xml or robots.txt
- **Fix:** Add `jekyll-sitemap` to `_config.yml` plugins (and a `robots.txt`). Currently `plugins: []`.

### 35. No skip-to-content link, no explicit focus styles
- **Where:** `default.html`, `style.css`
- **Fix:** Add a visually-hidden skip link at the top of `<body>` and explicit `:focus-visible` outlines on `.button`, `.card`, and nav links.

### 36. `--muted` (#527A8A) on white is right at the contrast edge
- **Where:** Body copy uses `--muted` in `.lead` and elsewhere.
- **Check:** Contrast ratio is approximately 4.4:1, borderline for WCAG AA on small text.
- **Fix:** Darken to ~#46697A or use full `--fg` for body text and reserve `--muted` for labels only.

### 37. Lexend font is loaded but unused
- **Where:** `default.html` Google Fonts URL
- **Fix:** Drop Lexend from the URL — it costs bytes for nothing.

### 38. Card hover changes background but cards aren't all links
- **Where:** `/services/` and `/about/` mix `.card` divs and `.card` anchors. Hover styling implies clickability even on non-link cards.
- **Fix:** Apply hover styling only to `a.card`, or make `.card` divs visually distinct from `a.card`.

### 39. `<details>` summary marker hidden via `list-style:none` and replaced with arrow pseudo-element
- **Where:** `style.css` lines 160–169
- **Issue:** Some assistive tech relies on the native disclosure triangle. Cosmetic replacement is fine but worth testing on VoiceOver/NVDA.
- **Fix:** Keep, but verify expansion is announced; alternatively use `details::marker` styling instead of removing it.

### 40. Site title font size of `34pt` may overflow at narrow widths
- **Where:** `style.css` `.site-title`
- **Issue:** `34pt` (~45px) on a header that already has a logo can wrap or push the nav off-screen on small phones.
- **Fix:** Use clamp: `font-size: clamp(22pt, 5vw, 34pt)`.

### 41. Goatcounter analytics is fine but no privacy/cookies copy anywhere
- **Where:** Footer
- **Note:** Goatcounter is cookie-free so a banner isn't legally required in most jurisdictions, but a one-line "We use cookieless analytics (Goatcounter)" link is a good signal for institutional partners.

---

## Summary: what to fix first

If you want to act on a small number of items and see disproportionate value:

1. **#1, #2, #3 (CERES, BETC, Jon Weaver titles)** — 10 minutes of edits, eliminates embarrassing errors.
2. **#4 (governance)** — 20 minutes, aligns the site with the funded proposal.
3. **#8, #9, #10 (lead, mission, "Why now")** — 30 minutes, transforms the homepage from generic to compelling.
4. **#15 (partners)** — biggest single message-vs-reality gap; even adding 10–12 named partners changes the page completely.
5. **#16/#17 (news)** — backfill 3 items, add to nav, or remove the page.

Everything else can flow from there. Let me know which items you want me to apply and I'll make the edits and produce a diff.
