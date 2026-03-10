# Content Strategy

How the site's content model is designed, what types of content exist, and how they work together to build topical authority and usability.

---

## Content Model

All content on ExpertNetworks.net is stored as JSON files in a Git repository. There is no CMS, no admin panel, and no database. The repository is the content management system.

### Provider Profiles (`src/content/networks/`)
- **Format:** One JSON file per provider (33 files)
- **Schema:** Validated by Zod at build time with 50+ defined fields
- **Scope:** Identity, services, pricing, compliance, AI capabilities, market positioning, confidence labels
- **Used by:** Directory, profiles, compare tool, pricing guide, search, footer, marquee

### News Signals (`src/content/news/`)
- **Format:** One JSON file per signal (57 files)
- **Schema:** Validated by Zod with required fields for title, date, source, significance, category
- **Scope:** Industry developments with source attribution and editorial context ("Why It Matters")
- **Used by:** News feed, homepage, provider profile pages (related news section)

### Compare Configuration (`src/content/compare.json`)
- **Format:** Single JSON file
- **Scope:** Default providers, 14 presets, section definitions, buyer pathways, contextual disclaimers
- **Used by:** Compare page (server-rendered defaults), compare controller (client-side state)

## Content Types and Their Roles

### Evergreen Educational Pages
- "What Is an Expert Network?" explainer
- Pricing guide
- Buyer guides (consulting, PE, hedge funds)

**Role:** Category education. These pages serve users who are new to expert networks or unfamiliar with specific aspects (pricing, compliance, AI). They remain relevant over time with periodic updates.

### Structured Provider Profiles
- 33 individual provider pages

**Role:** Provider-level depth. Each page provides a standardized, independent assessment that buyers can use during due diligence. Profiles are updated as new public information becomes available.

### Comparison Pages
- Dynamic compare tool
- 6 head-to-head comparison pages
- 3 alternatives pages

**Role:** Decision support. These pages assume the user has moved past discovery and into active evaluation. They show relationships between providers rather than describing providers individually.

### Pricing and Commercial Content
- Pricing guide with provider-level detail

**Role:** Commercial transparency. Addresses the single most-asked question in the expert network market: "How much does this cost?"

### Current-Awareness Content
- 57 news/intelligence signals

**Role:** Authority and relevance. Tracking industry developments signals that the site is actively maintained, provides value to repeat visitors, and builds topical depth.

### Rankings and Shortlists
- Top 15 ranking page

**Role:** Discovery and editorial authority. Rankings attract search traffic and give buyers a curated starting point. They require careful editorial framing.

### Trust and Methodology Pages
- About, Sources, Verification, Disclaimer, Privacy

**Role:** Credibility infrastructure. These pages answer the meta-question: "Why should I trust this site?"

## How Content Types Build Authority

The content strategy follows a hub-and-spoke topical model:

**Core topic:** Expert networks (the hub)
**Spokes:**
- Provider-by-provider coverage (33 profiles)
- Comparison content (dynamic tool + 9 static pages)
- Pricing content (dedicated guide)
- Industry news (57 signals)
- Educational content (explainer + buyer guides)
- Ranking content (top-15 list)

This breadth creates topical density. A search engine or a human evaluator can see that the site covers expert networks comprehensively — from definition through evaluation through current developments — rather than superficially.

## Content Quality Principles

### Specificity Over Generality
Provider descriptions cite specific services, founding dates, expert counts, and certifications rather than generic claims. "ISO 27001 certified as of January 2026" carries more weight than "strong security practices."

### Balance Over Promotion
Every provider profile includes both strengths and caveats. No provider is presented without critical context. This editorial balance is a key differentiator from vendor-controlled directories.

### Attribution Over Assertion
Where possible, claims are attributed to their source (provider website, press release, industry report). Where claims are editorial interpretation, they are labeled as such.

### Currency
News signals are datestamped. Provider profiles carry `lastUpdated` fields. Users can assess how current the information is rather than assuming it reflects the present.

## Content Governance

### Schema Enforcement
Zod schemas validate all content at build time. A provider JSON file with a missing required field or an invalid enum value will fail the build. This prevents structural inconsistencies from reaching production.

### Cross-Reference Integrity
News signals reference providers via slugs (`relatedNetworks` field). Provider profiles are linked from comparison presets, buyer pathways, and navigation elements. A post-build link checker validates all 8,800+ internal references.

### Editorial Review
Content changes are version-controlled in Git. The commit history provides a complete audit trail of what changed, when, and why.
