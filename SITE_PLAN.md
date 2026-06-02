# Site Guidance

Working principles for the BioHub website. Implementation history through May–June 2026 is preserved in git log; this file holds only the still-relevant guidance.

## Hedging principle

The BioHub has $5M MassTech funding (received Q1 2026), a Leadership Council, the BioLector hardware (in commissioning), and the existing WPI CERES capabilities. It does **not yet have:** the Pilot Facility, the Builder's Lab, the BioFoundry expansion, dedicated physical space beyond CERES, executed member contracts, or operational pilot fermentation.

Default voice across the site: **forward-looking, present-state-honest.** "Will feature" not "features." "Coming online over the next three years" not "operational." "Designed to support" not "supports." If a page describes a capability without hedging, treat it as a bug.

## Naming convention

- Default: **"the BioHub"** throughout.
- Use **"WPI–MBI BioHub"** when emphasizing the anchor partnership — About hero, Partners intro, partner-facing copy.
- Don't use "WPI BioHub" alone. It under-credits MBI.
- Reserve **"MassBioHub"** for the brand/URL form (`massbiohub.org`) only.

## Single contact point

Every CTA on the site — every "join the network," "get in touch," "stay informed" — routes to the same pre-filled `mailto:biohub@wpi.edu` template. There are **no separate signup forms, newsletter lists, or alternative addresses.** Audiences are differentiated by what they write in the email body, not by separate touchpoints.

The **"Following along"** card on Work With Us is the only mechanism for low-commitment contacts. Don't add "stay informed" to the engagement-interest options in the mailto body — that re-fragments the touchpoint.

## Voice / phrase audit

Avoid press-release filler that signals "skim me":
- **Cut:** "cutting-edge," "state-of-the-art," "innovation ecosystem"
- **Use sparingly:** "next-generation" (only if genuinely specific), "thriving" (soft enough to keep)
- **Keep when anchored:** "ecosystem" is fine when paired with a real noun ("regional bioindustrial ecosystem"). Cut when vague.

## Things explicitly decided NOT to do

- Add additional partners to the Partners page until Eric has vetted them.
- Add facility/equipment photography (infrastructure still being built).
- Add a Careers page (no openings to list yet).
- Add audience-routing cards beyond what's already on Work With Us.
- Use Plausible or GA4 for analytics (chose Goatcounter — cookieless).
- Surface DoD / SHIELD content on the public site.
- Surface tier names, fees, contract templates, or anchor-customer company names (Codomax / Holobiome / Literally Cotton) on the public site.
- Add a separate newsletter signup form (single-CTA principle).
- Build a standalone Visit page (deferred until the BioHub has dedicated physical space beyond CERES).
- Single out WPI ChemE alumni as their own audience-routing card (replaced with the generic "Following along" card).
- Mention Ecosystem Readiness Levels (ERL). MassTech-internal metric, not common knowledge for visitors.

## Deferred / waiting on input

- **Partners list expansion** — Eric to send a vetted set before adding to `_data/partners.yml`.
- **Photos for Jon Weaver and Liaohai Chen** — leadership cards currently asymmetric (only Eric has a portrait).
- **Homepage hero image** — first impression is still text-only; deferred until a usable photo exists.
- **OG image upgrade** — `assets/img/logos/og-default.png` is 847×630; should be 1200×630. The teal-canvas composite path is documented but not executed.
- **News backfill** — `news.md` is `published: false`; a scheduled task pings monthly to ask if there's anything to post.
- **Domain registrar** — `massbiohub.org` is now at Namecheap (transferred from Wix). Cloudflare wasn't a direct path; revisit moving it to Cloudflare for free DNS management when Namecheap's transfer lock lifts.
