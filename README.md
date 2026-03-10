# ExpertNetworks.net

**An independent, public-source research platform for comparing expert network providers.**

> Compare expert networks the way serious buyers actually evaluate them — by pricing, compliance posture, AI capabilities, transcript access, and service model.

**Live site:** [https://expertnetworks.net](https://expertnetworks.net/)

---

## Project at a Glance

| Dimension | Detail |
|-----------|--------|
| **What** | Independent research site covering the expert network industry |
| **Scope** | 33 providers tracked, 57 industry signals, 58 pages |
| **Stack** | Astro 5 (static), Tailwind CSS, TypeScript, Cloudflare Pages |
| **Content** | JSON-driven, Git-versioned — no CMS, no database |
| **Status** | Live and actively maintained |
| **Built by** | One person, end to end |

---

## Why This Project Exists

The expert network industry serves consulting firms, private equity, hedge funds, and corporate strategy teams — but public information about it is remarkably fragmented.

Provider websites lean toward marketing language. Pricing is rarely published. Compliance postures are described in broad strokes. AI capabilities are claimed but seldom compared. For a buyer evaluating which providers to engage, the practical information gap is significant.

This project exists to close that gap: a structured, independent, publicly accessible guide that organizes what is known about these providers into something a serious buyer can actually use.

No paid placements. No affiliations. No gated content. No login required.

---

## What the Site Covers

### Provider Directory
A browsable, filterable directory of 33 expert network providers with structured profiles covering services, pricing models, compliance posture, AI capabilities, scale, and market positioning.

### Side-by-Side Comparison Tool
A dynamic comparison experience supporting up to 6 providers across 29 structured data points — including pricing, compliance, AI workflow capabilities, delivery model, and scale. Preset comparisons by use case (consulting, private equity, AI-forward, transcript-led) offer immediate decision support.

### Pricing Guide
A detailed breakdown of expert network pricing in a market where most rates are negotiated privately. Covers per-call rates, subscription models, credit systems, cost drivers, and provider-specific pricing notes with confidence labeling.

### Industry Intelligence Feed
57 curated signals tracking acquisitions, funding rounds, product launches, partnerships, compliance certifications, and regulatory developments — organized by significance, category, and source type.

### Educational Content
A comprehensive explainer on what expert networks are, who uses them, how pricing works, and how to evaluate providers — designed for first-time buyers and non-specialists.

### Rankings and Buyer Guides
Editorially curated rankings (top 15 providers), industry-specific guides (consulting, PE, hedge funds), head-to-head comparisons (GLG vs AlphaSights, etc.), and alternatives pages.

### Trust Infrastructure
About, methodology, sources, verification, and disclaimer pages that frame the editorial approach: public-source research, per-field confidence labeling, corrections commitments, and clear separation of fact from inference.

---

## Who It Is For

- **Consulting teams** evaluating expert network partnerships
- **Private equity and hedge fund professionals** sourcing due diligence support
- **Corporate strategy teams** exploring research provider options
- **First-time buyers** trying to understand the category
- **Procurement teams** comparing compliance and pricing across providers
- **Anyone** looking for an independent view of this $2B+ industry

---

## Core Capabilities

- **Searchable provider discovery** with filtering by type, region, pricing model, delivery model, and capabilities
- **Dynamic side-by-side comparison** with presets for consulting, PE, AI-forward, and transcript-led workflows
- **Per-field confidence labeling** — verified, positioned, inferred, or estimated — across provider profiles
- **Buyer pathway navigation** linking use cases directly to relevant comparisons and providers
- **Industry signal tracking** with 57 curated articles classified by significance and category
- **Structured pricing transparency** covering 7 pricing models with provider-level detail
- **Head-to-head provider comparisons** (6 published) and alternatives pages (3 published)
- **JSON-LD structured data** on every page — BreadcrumbList, CollectionPage, FAQPage, Article, Organization
- **Full static build** — zero runtime backend, zero database, zero server dependencies
- **Accessibility-conscious design** — keyboard navigation, focus management, reduced-motion support, WCAG touch targets

---

## Page System Overview

| Page Type | Route | Purpose |
|-----------|-------|---------|
| Homepage | `/` | Entry hub with buyer pathways, featured providers, and current signals |
| Networks Directory | `/networks` | Browsable, filterable directory of all 33 tracked providers |
| Provider Profile | `/networks/[slug]` | Deep-dive profiles with services, compliance, AI, pricing, and related news |
| Compare Tool | `/compare` | Side-by-side comparison of up to 6 providers across 29 fields |
| Pricing Guide | `/expert-network-pricing` | Comprehensive pricing breakdown with confidence-labeled provider data |
| Industry Intelligence | `/news` | 57 curated signals with filtering by category, source, and significance |
| Explainer | `/what-is-an-expert-network` | Educational onboarding for first-time buyers |
| Best Networks | `/best-expert-networks` | Editorially curated top-15 ranking |
| Buyer Guides | `/expert-networks-for-*` | Industry-specific guides for consulting, PE, and hedge funds |
| VS Comparisons | `/glg-vs-alphasights`, etc. | Head-to-head provider comparisons (6 pages) |
| Alternatives | `/glg-alternatives`, etc. | Provider alternative recommendations (3 pages) |
| About | `/about` | Purpose, methodology overview, editorial philosophy |
| Sources | `/sources` | Four-tiered evidence framework and confidence labeling system |
| Verification | `/verification` | Build-time validation approach and known limitations |
| Disclaimer | `/disclaimer` | Legal framing, MNPI guidance, accuracy caveats |

---

## Information Design Principles

The site is designed around a set of editorial and UX commitments:

- **Trust before promotion.** Every page leads with what is known and how it is known, not with marketing claims.
- **Public-source transparency.** All information is drawn from publicly available materials. The sourcing approach is documented on the site.
- **Compare-first usability.** The comparison tool is central — not an afterthought bolted onto a directory.
- **Buyer-pathway orientation.** Multiple entry points by role (consulting, PE, hedge funds) and by workflow (fast calls, transcript research, AI sourcing).
- **Confidence labeling.** Claims are tagged per-field as verified, positioned, inferred, or estimated — because not all information carries equal weight.
- **No gatekeeping.** No login, no paywall, no email capture requirement. The information is public.
- **Careful distinction.** Rankings and comparisons are framed as editorial interpretation, not objective truth. Disclaimers are built into the content, not buried in footnotes.

---

## What This Project Demonstrates

This is an independently conceived, researched, designed, and shipped information product. As portfolio evidence, it demonstrates:

- **Product strategy** — identifying a real information gap in a niche market and designing a multi-page system to address it
- **Information architecture** — structuring 33 providers, 57 signals, and 15+ page types into a coherent, navigable system
- **Taxonomy design** — building a classification system (type, delivery model, compliance badge, AI badge, pricing model, region strength) that supports filtering, comparison, and discovery
- **Content system thinking** — designing a JSON-driven content model with Zod validation, cross-reference integrity, and per-field confidence labeling
- **Frontend execution** — static site generation with Astro, client-side interactivity (comparison tool, search, filtering), canvas-based animations, and responsive design
- **Editorial discipline** — maintaining consistent tone, careful framing of uncertainty, and trust infrastructure across 58 pages
- **SEO-conscious structuring** — query-aligned page types, structured data (JSON-LD), internal cross-linking, and topical authority through comprehensive category coverage
- **Trust and credibility awareness** — designing for skeptical professional audiences where credibility is earned through transparency, not claimed through assertion
- **Niche market research** — synthesizing fragmented public information about 33 providers into a structured, comparable format
- **Independent execution** — built end-to-end by one person, from market research through content creation, design, development, and deployment

---

## Technical Architecture

```
                    ┌─────────────────────┐
                    │    Astro (Static)    │
                    │  Build-time render   │
                    └────────┬────────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────▼──┐    ┌─────▼─────┐   ┌────▼──────┐
     │  Content   │    │   Pages   │   │Components │
     │  (JSON)    │    │  (.astro) │   │  (.astro) │
     └────────┬──┘    └─────┬─────┘   └────┬──────┘
              │              │              │
              │    ┌─────────▼──────────┐   │
              └────▶  Built HTML/CSS/JS ◀───┘
                   └─────────┬──────────┘
                             │
                   ┌─────────▼──────────┐
                   │  Cloudflare Pages   │
                   │  (Static hosting)   │
                   └────────────────────┘
```

**Content model:** JSON files in `src/content/` — one per provider, one per news item — validated at build time by Zod schemas.

**No runtime backend.** The site is fully static. Client-side JavaScript handles comparison tool state, search overlay, filtering, and animations. URL parameters make comparison states shareable.

**Validation pipeline:** `npm run verify` runs the full build, checks all 8,800+ internal links, and runs TypeScript validation.

---

## Repository Guide

```
/
├── README.md                         # This file
├── CONTRIBUTING.md                   # Contribution guidelines
├── CHANGELOG.md                      # Release history
├── LICENSE                           # MIT License
├── docs/
│   ├── overview.md                   # Project orientation
│   ├── project-story.md              # Origin and motivation
│   ├── site-architecture.md          # System design and page relationships
│   ├── feature-system.md             # Feature-by-feature breakdown
│   ├── page-guide.md                 # Detailed page-by-page documentation
│   ├── methodology-and-standards.md  # Research and editorial standards
│   ├── product-decisions.md          # Design rationale and tradeoffs
│   ├── ux-and-information-design.md  # Information architecture and UX logic
│   ├── content-strategy.md           # Content model and editorial approach
│   ├── seo-discoverability.md        # Search strategy and structured data
│   ├── roadmap.md                    # Planned improvements
│   ├── faq.md                        # Common questions
│   └── assets/
│       └── README.md                 # Screenshot guidance
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── bug_report.md
    │   ├── feature_request.md
    │   └── documentation.md
    └── PULL_REQUEST_TEMPLATE.md
```

---

## Screenshots

> Screenshots of the live site are planned for this repository. See [`docs/assets/README.md`](docs/assets/README.md) for the visual documentation roadmap.

| Screenshot | Description |
|-----------|-------------|
| `homepage-hero.png` | Homepage with particle hero and buyer pathways |
| `networks-directory.png` | Provider directory with filters and cards |
| `provider-profile.png` | Individual provider deep-dive page |
| `compare-tool.png` | Side-by-side comparison with 6 providers |
| `pricing-guide.png` | Pricing breakdown with confidence labels |
| `news-feed.png` | Industry intelligence feed with filters |
| `mobile-responsive.png` | Mobile layout across key pages |

---

## How to Explore

If you are reviewing this project, here is the recommended order:

1. **Visit the live site** — [expertnetworks.net](https://expertnetworks.net/)
2. **Try the comparison tool** — [/compare](https://expertnetworks.net/compare) — switch presets and add/remove providers
3. **Browse the directory** — [/networks](https://expertnetworks.net/networks) — try filters and search
4. **Read a provider profile** — [/networks/glg](https://expertnetworks.net/networks/glg) — see the depth of structured data
5. **Check the pricing guide** — [/expert-network-pricing](https://expertnetworks.net/expert-network-pricing) — note the confidence labels
6. **Scan the news feed** — [/news](https://expertnetworks.net/news) — filter by category or significance
7. **Read the methodology** — [/sources](https://expertnetworks.net/sources) — understand the evidence framework
8. **Review this repository** — start with [`docs/overview.md`](docs/overview.md), then [`docs/page-guide.md`](docs/page-guide.md)

---

## Current Status

The site is live and actively maintained. Content is updated as new public information becomes available — provider developments, industry signals, pricing changes, and compliance updates.

This repository contains portfolio-oriented documentation that explains the project's scope, architecture, design decisions, and editorial standards. The source code lives in a separate private repository.

---

## Roadmap

See [`docs/roadmap.md`](docs/roadmap.md) for the full improvement plan. Key directions:

**Now:** Richer provider profiles, additional news coverage, stronger visual documentation in this repository.

**Next:** Enhanced comparison logic, additional buyer guides, improved mobile comparison experience, deeper compliance and AI capability tracking.

**Later:** Automated news monitoring, expanded provider coverage, richer data visualization.

---

## License

This project is available under the [MIT License](LICENSE). Content, editorial framing, and research are original work. Provider data is drawn from public sources and attributed accordingly.

---

<p align="center">
  <a href="https://expertnetworks.net">expertnetworks.net</a> · Independent expert network research
</p>
