# Massachusetts BioHub website — ledger.md

## Tasks

Last verified against the rendered pages: 2026-08-22. Open work first; settled decisions below it as one-liners so they are not re-litigated. **Do not let this section grow back into a narrative** — the how-we-got-here lives in git log.

### Open — mine

- [ ] **SEC 1 — repo is public and tracks `CLAUDE.md` and `SITE_PLAN.md`** (verified 2026-10-18 via GitHub API). `.gitignore` was added after they were committed, so it ignores nothing. Values, anchor-customer names, the BPC note, and the OneDrive path are all readable on GitHub, and history also holds `AUDIT.md` with 17 company names. Private is out because the repo serves Pages (Eric, 2026-10-18). History purged and force-pushed 2026-10-18 (683382e, 0 leak hits, both files 404 on GitHub). **Remaining:** old commits are still reachable by SHA, so ask GitHub Support ("Remove sensitive data") to purge cached views and dangling commits. Brand and facts are mirrored to the private BioHub Claude project; `CLAUDE.md` and `SITE_PLAN.md` exist only locally.
- [x] **SEC 2a — `massbiohub.org` verified in GitHub Pages** (2026-10-18; TXT `_github-pages-challenge-yoeric` is live). Keep the record.
- [x] **SEC 2b — CI token is `contents: read`** (2026-10-18).
- [ ] **FACT — Builder's Lab 4,500 sq ft confirmed by Eric 2026-10-18.** The public ~15,000 sq ft figure covers all of 17 Briden St., so keep 4,500. Still open: the "10,000 sq ft pilot facility" (`services.md:61`) has no public source. Confirm both with Eric/MBI. BETC 3,000+ and the McKinsey "per year" wording have no public source but are settled (see below), so keep the internal source on file.
- [x] **UX 1 — inquiry address now shown as text in the Contact lead** (2026-10-18).
- [x] **PERF — WPI logo 649 KB → 27 KB; every `<img>` has width/height** (2026-10-18).
- [x] **ARCH — repeated facts moved to `_data/facts.yml`, leadership to `_data/people.yml`** (2026-10-18; rendered text diffed identical against the prior build). Scale figures move with the MERGE into a services data file.
- [x] **PLACEHOLDER — cut to three pages, Home · About · Contact (Eric, 2026-10-18).** Services, Partners, and Work With Us are deleted, and their URLs redirect via `jekyll-redirect-from`. This carries out the MERGE decision in reduced form: card 1 covers infrastructure and process development, card 2 is Builder's Lab only. It also closes UX 2 (the three-item nav fits on a phone), COPY E (card 1 contradiction, unhedged descriptions, "three years" phrasing), COPY A, and COPY D. A navy "Partner with us" band on Home and a partnership CTA on About keep partnering prominent.
- [ ] **Deferred to the launch site, not the placeholder:** CEO 3–8 (surfacing CERES equipment, a named human on Contact, a network referral offer, a pricing model, IP/CDA language for startups, and a yield frame for 100 L). The pre-cut `services.md` (equipment lists, planned specs) is in git history for reuse at launch.

### Code audit — done 2026-10-04

Verified by local build and a computed-style diff of all pages against the pre-audit build. The rules it produced live in Design System and Architecture above.

- [x] **Four unused images deleted** (2026-10-18).

### Open — Eric

- [x] **Serve it.** Local `bundle exec jekyll build --future` passes clean (2026-10-04).
- [x] **Delete before committing:** the four `*_white.png` logos and `_to_delete/` deleted 2026-10-04 (both were tracked in git — commit the deletions). `biohub_logo_transparent.png` kept: the JSON-LD points at it.
- [x] **OG image is 1200×630** (verified 2026-10-18). The `SITE_PLAN.md` deferred item is stale.
- [ ] **Mockup artifact is stale** — shows the teal-on-white draft. Only matters if that URL was shared.

### Settled — do not re-litigate

- **Governance is a Governing Board, supported by an Advisory Group**, made up of WPI, MBI, MassTech, and stakeholders. Established by executed charters. The June `AUDIT.md` "corrected" this to Leadership Council from the proposal; that was wrong. **Charter beats proposal, always.**
- **NSF wording is "Part of one of five NSF BioFoundries in the country."** The site once claimed WPI *was* one of the five leads; NSF's award list contradicts that. Federal stat tile reads "NSF BioFoundry" with no dollar figure, by Eric's choice.
- **Scale range is 100 µL–100 L** — BioFoundry 100 µL–500 mL, Pilot Facility 1 L, 10 L, 100 L. Supersedes the proposal's 2L–150L.
- **Every rung of the ladder runs today (2026-08-22).** The **WPI Bioprocess Center** at **60 Prescott Street** already operates a **100 L Sartorius fermenter** and **BioFlo 3000s at 1 L, 5 L, and 10 L** working volume, plus TFF, pilot homogenizer, pilot lyophilizer, and an Agilent 1200 HPLC, offered as contract microbial fermentation. So 1 L–100 L is **not** "in build-out" and must never again be drawn that way. What the BioHub adds at that span is **shared** capacity — instrumented, anaerobic-capable, bookable without a WPI research relationship. Equipment list is from BPC's own site (`biopc.wpi.edu/projects/`, read 2026-08-22); Eric notes usage is low, and their director died, so **re-verify before leaning on it further**.
- **BPC inquiries route through `biohub@wpi.edu`, never to BPC directly.** Their throughput is limited; the site names the capability but points every inquiry at Eric to triage. Do not add a BPC phone, address-linked contact, or staff name anywhere on the site.
- **BPC's downstream is pharma-oriented** — TFF, homogenization, lyophilization. Bioindustrial products are high volume at lower unit value and need evaporation, spray drying, and membrane filtration at scale instead. **This is the Pilot Facility's sharpest differentiator** and beats "shared access" as an argument. Eric, 2026-08-22. It carries the Builder's Lab too: a startup building bioindustrial separation, evaporation, or drying equipment has nowhere regional to test it against real broth at volume, and the Pilot Facility supplies the broth. Stronger than "prototyping space."
- **Three Gateway Park buildings, not two:** **50 Prescott** (BETC, CERES/BioFoundry, Pilot Facility), **60 Prescott** (Bioprocess Center), **17 Briden** (MBI Builder's Lab). The site's own address and schema stay 50 Prescott. "Under one roof" and "one campus" remain banned; the approved framing is "in Worcester".
- **Leadership block:** Young (Director · Principal Investigator), Weaver (Regional Innovation Officer), Chen (Co-Principal Investigator). No "Pilot Facility Lead", no PracticePoint — do not re-add either from WPI's directory.
- **"35+" partners rests on Eric's knowledge, not a document** — the proposal says both 33 and 35. Re-verify before partner-facing use.
- **News is dropped** — `news.md`, `news.yml`, and the include are gone. Do not rebuild it.
- **Values are internal only.** Brand story is public and lives on About.
- **The mission keeps present tense; the homepage hedges.** `/about/` Mission reads "The BioHub **gives** companies…"; the `index.md` lead reads "**will give**". Deliberate, decided 2026-08-22 — the mission is a statement of purpose, the homepage lead is site copy bound by the hedging rule. Do not "reconcile" these.
- **Corrected claims now live on the site** — CBRE talent ranking replacing an unsupported BLS claim, McKinsey figure with "per year" restored, $5.2M, 50 Prescott, BETC "first 11 years", Department of War attribution. Do not revert any of these to their earlier wording.
