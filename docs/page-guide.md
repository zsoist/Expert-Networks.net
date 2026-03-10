# Page Guide

A detailed walkthrough of every major page type on ExpertNetworks.net — its purpose, structure, content logic, and role in the overall system.

---

## Homepage

**Route:** `/`
**User intent:** "I want to understand what this site offers and find the right starting point."

### Purpose
The homepage functions as a routing layer. Rather than overwhelming visitors with data, it presents structured entry points to the site's main systems: directory, comparison tool, pricing guide, news feed, and educational content.

### Key Modules
1. **Hero** — Typewriter-animated headline with interactive particle canvas. Sets the editorial tone: "Compare expert networks the way serious buyers actually evaluate them."
2. **Trust strip** — Three proof points: providers tracked, public-source research, no affiliations. Establishes credibility immediately.
3. **Provider marquee** — Horizontally scrolling carousel of all 33 tracked provider logos. Hover cards show expert count, pricing model, and description.
4. **Decision pathways** — Six cards linking to buyer-specific starting points: Consulting Teams, PE & Hedge Funds, Enterprise Strategy, Transcript-Led, AI-Forward, First-Time Buyer.
5. **Compare module** — Three featured comparison presets (Leaders, AI-Forward, Library-Heavy) with direct links.
6. **Featured profiles** — Top 6 providers by editorial priority.
7. **Current signals** — 3 most recent major/standard news items.
8. **Methodology summary** — Brief explanation of the site's research approach.
9. **Final CTA** — Link to the comparison tool.

### Trust Framing
The homepage leads with independence ("No paid placements") before showing any provider data. This ordering is deliberate — credibility comes before content.

### Portfolio Relevance
Demonstrates: information hierarchy, user routing logic, visual design judgment, trust-first editorial framing.

---

## Networks Directory

**Route:** `/networks`
**User intent:** "I want to browse and discover expert network providers."

### Purpose
The directory serves buyers who do not yet have a shortlist. It enables exploration through filtering, search, and visual browsing rather than forcing users to read sequential profiles.

### How Filtering Supports Discovery
Filters are organized into four groups:

- **Fit** — Region strength, provider type
- **Commercial Model** — Pricing model, delivery model, HQ location
- **Capabilities** — AI matching, compliance tools, surveys, content library
- **Sort** — Default rank, alphabetical, founding date

This taxonomy was designed around the questions buyers actually ask during evaluation, not around provider self-classification.

### Card Information
Each provider card shows: name, logo, category badge, description excerpt, pricing model, expert count, founding year, delivery model, key service icons, and compare checkbox. Users can build a comparison selection directly from the directory.

### Search
Real-time search filters providers by name as the user types. The global search overlay (accessible from any page via `/` key) also covers the full provider set.

### Mobile Behavior
On mobile, filters collapse behind a toggle button with `aria-expanded` state management. The compare tray appears at the bottom of the viewport when selections are made.

### Portfolio Relevance
Demonstrates: taxonomy design, filtering UX, card-based information density, mobile-responsive layout, compare integration.

---

## Provider Profiles

**Route:** `/networks/[slug]` (33 pages)
**User intent:** "I want to evaluate this specific provider in detail."

### Purpose
Each provider page presents structured, independent information organized around the questions a buyer would ask during due diligence.

### Content Sections
- **Hero** — Provider name, type badge, compliance badge, AI badge, key metrics (founded, HQ, experts, employees)
- **Overview** — Description and market positioning
- **Services** — List or accordion of service offerings
- **Pricing** — Model, detail, and confidence label
- **Best For** — Target buyer segments
- **Strengths & Caveats** — Balanced assessment with specific points
- **Deep Dive** (rich profiles only):
  - History with timeline events
  - Industry coverage
  - Client fit analysis
  - AI platform description with specific features
  - Extended compliance analysis with regulatory context
  - Notable facts and source notes
- **Confidence Badges** — Per-field labels (verified, positioned, inferred, estimated)
- **Related News** — Up to 5 recent signals mentioning this provider

### Sidebar Navigation
Desktop profiles include a sticky right-side table of contents for quick section navigation. The sidebar also shows links to relevant comparison pages, alternatives pages, and the main comparison tool.

### Portfolio Relevance
Demonstrates: structured data presentation, confidence labeling UX, cross-reference integration (news → profile → compare), editorial balance (strengths and caveats).

---

## Compare Tool

**Route:** `/compare`
**User intent:** "I need to evaluate these specific providers against each other."

### Purpose
The comparison tool is the site's central decision-support instrument. It places providers side by side across 29 structured dimensions so buyers can see exactly where providers differ and where they overlap.

### Decision-Support Role
The compare page assumes the user has moved past discovery and into evaluation. Rather than describing providers individually, it shows how they relate to each other on specific criteria.

### Why Presets Matter
14 named presets address a common problem: users who know their use case but not which providers to compare. Presets like "Best for Private Equity" or "Transcript Leaders" provide informed starting points.

### Comparison Dimensions (5 categories, 29 fields)
1. **Core Offering** — Type, expert calls, surveys, content library, compliance tools, delivery model
2. **AI & Workflow** — Expert matching, transcript Q&A, synthesis, workflow automation, AI interviewing, compliance AI
3. **Commercial** — Pricing model, geography, scale
4. **Scale** — Expert count, employees, founding date, HQ
5. **Compliance** — MNPI policy, vetting, audit trail, cooling-off period

### Interactive Features
- Add/remove up to 6 providers via search modal
- Diff mode (show only differences)
- Evidence notes toggle (show confidence levels)
- Goal-based filtering (fast calls, AI sourcing, lowest compliance risk)
- URL state synchronization for shareable comparisons

### Portfolio Relevance
Demonstrates: complex client-side state management, URL-driven application state, preset-based UX, information density in tabular format, accessibility in interactive components.

---

## Pricing Guide

**Route:** `/expert-network-pricing`
**User intent:** "How much do expert networks cost, and what drives the price?"

### Purpose
Expert network pricing is almost entirely negotiated and rarely published. This page turns an opaque market into a structured education resource.

### Content Structure
1. **Executive summary** — 3 key metrics (call rate range, expert compensation range, B2B survey response rate)
2. **7 pricing models explained** — Per-call, credit-based, subscription, project-based, hybrid, platform fee, custom
3. **Provider pricing table** — All 33 providers with model, specific notes, and confidence level
4. **8 cost drivers** — Seniority, urgency, geography, compliance, exclusivity, format, volume, scope
5. **Buyer framework** — Recommendations by organization type
6. **Negotiation guidance** — Tactics and red flags

### Confidence Labels in Context
The pricing table applies the confidence labeling system to each provider's pricing information. Some providers publish rates (verified). Some describe ranges in marketing (positioned). Some pricing data comes from third-party benchmarks (inferred). Some providers publish nothing (not disclosed). This transparency helps buyers calibrate their expectations.

### Portfolio Relevance
Demonstrates: turning opaque information into a usable resource, confidence-based data presentation, editorial care in a commercially sensitive area.

---

## Industry Intelligence Feed

**Route:** `/news`
**User intent:** "What's happening in the expert network industry?"

### Purpose
The news feed tracks industry developments — acquisitions, funding, product launches, partnerships, compliance certifications, regulatory actions — in a curated, categorized format.

### Signal Classification
- **Significance:** Major (market-moving), Standard (noteworthy), Brief (minor or contextual)
- **Category:** AI, Compliance, Culture, Expansion, Funding, IPO, Industry, Leadership, Legal, M&A, Market Data, Partnerships, Product, Research, Technology
- **Source type:** Press Release, Industry Report, News Coverage, Product Update, Regulatory

### Filters
Category, network, source type, time range, significance level, and sort order. Filter state persists to URL parameters for sharing.

### Portfolio Relevance
Demonstrates: content curation, classification system design, filter-driven UX, URL state persistence.

---

## What Is an Expert Network? Explainer

**Route:** `/what-is-an-expert-network`
**User intent:** "I'm new to this — explain the category."

### Purpose
Onboards users who are unfamiliar with the expert network concept. Covers the full range of questions a first-time buyer would ask: definition, legality, cost, typical users, services, compliance considerations, and how to choose a provider.

### Content Logic
The page follows a progressive structure: define → contextualize → educate → guide. It starts with what expert networks are, moves through who uses them and what they cost, addresses compliance concerns (including the historical context of insider trading cases), and ends with practical selection criteria.

### Trust Function
By covering compliance and legal history openly, the page builds credibility. Many provider websites downplay or omit this context. Including it signals editorial maturity.

### Portfolio Relevance
Demonstrates: educational content design, progressive disclosure, sensitive topic handling, FAQ schema implementation.

---

## Best Expert Networks Ranking

**Route:** `/best-expert-networks`
**User intent:** "What are the top expert networks?"

### Purpose
Rankings attract discovery (especially from search) and give buyers a curated starting point. The page ranks the top 15 providers with category groupings and delivery model breakdowns.

### Nuance and Disclaimers
Rankings require careful framing. The page:
- Discloses the criteria used (scope, compliance, AI investment, market presence)
- States that no affiliations or sponsorships influence the ranking
- Groups providers by category (Global Leaders, Fast-Growing, Specialized) to avoid implying a single linear hierarchy
- Links each ranked provider to their full profile for deeper evaluation

### Portfolio Relevance
Demonstrates: editorial judgment, responsible ranking methodology, SEO-conscious content design, trust-aware framing.

---

## Head-to-Head Comparisons

**Routes:** `/glg-vs-alphasights`, `/glg-vs-third-bridge`, `/glg-vs-guidepoint`, `/alphasights-vs-third-bridge`, `/alphasights-vs-dialectica`, `/third-bridge-vs-guidepoint`
**User intent:** "How does [Provider A] compare to [Provider B]?"

### Purpose
These pages address specific, high-intent search queries. Users searching "GLG vs AlphaSights" have already narrowed their evaluation to two providers and want a direct comparison.

### Content Logic
Each page uses a structured two-column layout comparing providers across key attributes: type, delivery model, compliance posture, AI capabilities, pricing model, scale, and editorial assessment. A verdict section at the bottom synthesizes the comparison.

### Portfolio Relevance
Demonstrates: query-aligned content strategy, structured comparison UX, editorial synthesis.

---

## About / Sources / Disclaimer

**Routes:** `/about`, `/sources`, `/disclaimer`, `/verification`, `/privacy`
**User intent:** "Can I trust this site? Where does the information come from?"

### Purpose
Trust infrastructure for a site that makes claims about a $2B+ industry. These pages explain the editorial approach, evidence system, known limitations, and legal framing.

### Why It Matters
Professional audiences — especially in finance and consulting — are trained to evaluate sources critically. The trust pages preempt the question "Who is behind this and what's their angle?" with transparent answers.

### Sources Page
Documents the four-tiered evidence framework, confidence labeling system, and corrections approach. This is not a formality — it is a core differentiator of the site.

### Portfolio Relevance
Demonstrates: credibility-aware design, transparency as a product feature, maturity in handling editorial independence.
