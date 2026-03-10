# Feature System

A breakdown of the site's major features — what each one does, why it exists, and what user problem it addresses.

---

## Searchable Provider Discovery

**What it does:** A browsable directory of 33 expert network providers with card-based layout, real-time search, and multi-dimensional filtering.

**Filters available:**
- Provider type (Pure-Play, Hybrid, AI Platform, Research Platform)
- Region strength (Global, Asia-Pacific, Europe)
- Pricing model (Per-call, Subscription, Credit-based, Platform fee)
- Delivery model (Concierge, Marketplace, Platform-Led, Self-Serve)
- HQ location (by country)
- Capabilities (AI Matching, Compliance Tools, Surveys, Content Library)
- Sort order (default rank, alphabetical, founding date)

**Why it exists:** Buyers entering the expert network market often do not know which providers are relevant to them. A filterable directory lets them narrow the field based on criteria they care about rather than reading through 33 profiles sequentially.

**User problem it solves:** "I need to find expert network providers that match my requirements."

---

## Provider Profiles

**What it does:** Individual pages for each provider with structured data sections: overview, services, pricing, compliance, AI capabilities, client fit, strengths, caveats, and related industry signals. Rich profiles include history timelines, detailed service breakdowns, and notable facts.

**Per-field confidence badges:** Each data point is tagged as verified, positioned, inferred, or estimated — so users know how much weight to place on each claim.

**Why it exists:** Marketing-oriented provider websites do not present information in a standardized, comparable format. These profiles restructure public information around the questions buyers actually ask.

**User problem it solves:** "I need a structured, independent view of this specific provider."

---

## Side-by-Side Comparison Tool

**What it does:** A dynamic comparison interface placing up to 6 providers next to each other across 29 structured dimensions, organized into 5 categories:

1. **Core Offering** — provider type, expert calls, surveys, content library, compliance tools, delivery model
2. **AI & Workflow Stack** — expert matching, transcript Q&A, synthesis, workflow automation, compliance AI
3. **Commercial Model** — pricing model, geography, scale indicators
4. **Scale & Coverage** — expert count, employee count, founding date, headquarters
5. **Compliance & Governance** — MNPI policies, vetting procedures, audit trails, cooling-off periods

**Interactive features:**
- Add/remove providers via search modal
- 14 named presets by use case (consulting, PE, AI-forward, transcript-led, healthcare, APAC, etc.)
- Diff mode (show only columns where providers differ)
- Evidence notes toggle (show confidence levels inline)
- URL synchronization (shareable comparison states)

**Why it exists:** Directories show individual providers. Comparisons show relationships between providers. The compare tool is the central decision-support instrument of the site.

**User problem it solves:** "I need to evaluate these specific providers against each other on the criteria I care about."

---

## Preset-Based Comparisons

**What it does:** 14 named presets pre-select providers relevant to specific buyer scenarios:

- Global Leaders, PE/Hedge Funds, Consulting Fit
- Transcript Leaders, AI Research, AI-Forward
- APAC Specialists, Europe Markets, Healthcare
- Fast Calls, Public Markets, NA Platform

**Why it exists:** Many buyers do not yet have a shortlist. Presets give them an informed starting point based on their industry or workflow, rather than requiring them to build a comparison from scratch.

**User problem it solves:** "I don't know which providers to compare — show me the relevant ones for my situation."

---

## Pricing Transparency

**What it does:** A dedicated pricing guide covering:

- 7 pricing models explained (per-call, credit-based, subscription, project-based, hybrid, platform fee, custom)
- Market rate ranges (standard calls ~$700–$1,500+/hr, expert compensation $200–$500+/hr)
- All 33 providers tabled with their pricing model, specific notes, and confidence level
- 8 cost drivers analyzed (seniority, urgency, geography, compliance, exclusivity, format, volume, scope)
- Buyer framework by organization type
- Negotiation guidance

**Why it exists:** Expert network pricing is almost entirely negotiated. Providers rarely publish rates. This creates an information asymmetry that disadvantages first-time buyers. The pricing guide turns opaque pricing into a structured education resource.

**User problem it solves:** "How much do expert networks cost, and what drives the price?"

---

## Industry Intelligence Feed

**What it does:** A curated feed of 57 industry signals covering:

- Acquisitions, funding rounds, IPOs
- Product launches, partnerships
- Compliance certifications, regulatory developments
- Market data and industry projections

**Classification system:**
- **Significance:** Major, Standard, Brief
- **Category:** AI, Compliance, Expansion, Funding, M&A, Product, Technology, etc.
- **Source type:** Press Release, Industry Report, News Coverage, Product Update, Regulatory

**Filters:** Category, network, source type, time range, significance level, sort order. Filter state persists to URL for sharing.

**Why it exists:** The expert network market is consolidating and evolving rapidly. Tracking developments helps buyers understand which providers are growing, which are investing in AI, and where the market is heading.

**User problem it solves:** "What's happening in the expert network industry right now?"

---

## Educational Content

**What it does:** A comprehensive explainer page covering:

- What expert networks are and how they work
- Who uses them (PE, consulting, corporate strategy, legal)
- Services available (calls, surveys, events, libraries, placements)
- How pricing works
- Compliance and legal considerations
- How to choose a provider
- How expert networks compare to alternatives

**Why it exists:** The term "expert network" is not universally understood. First-time buyers, adjacent professionals, and procurement teams need category-level education before they can evaluate specific providers.

**User problem it solves:** "What is an expert network, and should my team be using one?"

---

## Rankings and Shortlist Pages

**What it does:** An editorially curated ranking of the top 15 expert networks, plus head-to-head comparison pages (6 published) and alternatives pages (3 published).

**Ranking criteria:** Network size, global reach, product breadth, compliance maturity, AI investment, market share.

**Why it exists:** Rankings attract discovery and give buyers a curated starting point. The editorial framing is important — rankings are presented as interpretation, not objective measurement, with appropriate caveats.

**User problem it solves:** "What are the best expert networks? Who are the main alternatives to [provider]?"

---

## Trust and Methodology Infrastructure

**What it does:** A set of pages that establish editorial credibility:

- **About** — purpose, editorial philosophy, independence statement
- **Sources & Methodology** — four-tiered evidence system (primary sources, independent reporting, company-originated content, editorial synthesis)
- **Verification** — build-time validation approach, cross-reference integrity
- **Disclaimer** — legal framing, MNPI guidance, accuracy caveats
- **Privacy** — data collection practices (minimal — public-source research only)

**Confidence labeling system:**
- **Verified** — confirmed by the provider or an independent public source
- **Positioned** — provider marketing claim, not independently verified
- **Inferred** — based on third-party benchmarks or market reporting
- **Estimated** — directional, based on incomplete data

**Why it exists:** An independent site making claims about an industry needs to be transparent about how those claims are supported. Professional audiences are skeptical by default — trust infrastructure reduces that skepticism.

**User problem it solves:** "Can I trust this information? Where does it come from?"

---

## Global Search

**What it does:** A full-screen search overlay (triggered by `/` keyboard shortcut or header icon) that searches across all 33 providers with real-time filtering. Results show provider name, type badge, and direct links to profiles.

**Why it exists:** Users with a specific provider in mind should be able to find it instantly without navigating through the directory.

**User problem it solves:** "I need to find a specific provider quickly."

---

## Buyer Pathway Navigation

**What it does:** Role-based and workflow-based entry points throughout the site:

- **By buyer type:** Consulting Teams, PE & Hedge Funds, Enterprise Strategy
- **By workflow:** Fast Calls, Transcript-Led Research, AI Sourcing, Compliance-Heavy

These pathways link to relevant comparison presets, provider filters, and buyer guides.

**Why it exists:** Different buyer types prioritize different criteria. A PE firm cares most about compliance and fast turnaround. A consulting team cares about scale and breadth. Pathways route users to the most relevant starting point.

**User problem it solves:** "I'm a [role] — what matters for me?"
