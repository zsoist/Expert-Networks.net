# Site Architecture

## System Overview

ExpertNetworks.net is a static site built with Astro, hosted on Cloudflare Pages. All content is stored as JSON files validated by Zod schemas at build time. There is no runtime backend, no database, and no CMS.

The site is organized as an interconnected system of page types, each serving a distinct role in the buyer's information journey.

## Page Type Map

```
                         ┌──────────┐
                         │ Homepage │
                         │  (Hub)   │
                         └────┬─────┘
                              │
            ┌─────────────────┼─────────────────┐
            │                 │                 │
     ┌──────▼──────┐   ┌─────▼─────┐   ┌──────▼──────┐
     │  Directory   │   │  Compare  │   │    News     │
     │ (Discovery)  │   │(Evaluate) │   │ (Monitor)   │
     └──────┬──────┘   └─────┬─────┘   └─────────────┘
            │                 │
     ┌──────▼──────┐   ┌─────▼─────┐
     │  Provider   │   │  Presets   │
     │  Profiles   │   │ VS Pages  │
     └─────────────┘   │ Alt Pages │
                       └───────────┘

     ┌─────────────┐   ┌───────────┐   ┌─────────────┐
     │   Pricing   │   │ Explainer │   │    Trust     │
     │   Guide     │   │  Content  │   │   Pages     │
     └─────────────┘   └───────────┘   └─────────────┘
```

## Page Types and Their Roles

### Homepage — Entry Hub
The homepage routes users to the right starting point. It does not try to show everything; it offers structured pathways:

- **Buyer pathways** by role (consulting, PE, hedge funds) and by workflow (fast calls, transcripts, AI sourcing)
- **Featured providers** surfacing the highest-priority profiles
- **Current signals** showing the latest industry developments
- **Compare entry points** with preset shortcuts

### Networks Directory — Market Browsing Layer
The directory enables open-ended exploration. Users who do not yet have a shortlist can filter by type, region, pricing model, delivery model, or capabilities. The directory supports both card and list views, with search and sort.

### Provider Profiles — Depth Layer
Each provider has a dedicated page with structured sections: services, pricing, compliance, AI capabilities, strengths, caveats, and related news. Rich profiles include timelines, detailed service descriptions, and confidence badges per field.

### Compare Tool — Decision-Support Layer
The compare page places providers side by side across 29 structured dimensions. Users can select up to 6 providers, apply presets by use case, toggle diff mode (show only differences), and view evidence notes with confidence levels. URL parameters make any comparison state shareable.

### Pricing Guide — Commercial Transparency Layer
A standalone page covering 7 pricing models, market rate ranges, cost drivers, and provider-specific pricing notes. Each provider's pricing is tagged with a confidence level.

### Industry Intelligence — Current-Awareness Layer
The news feed tracks 57 curated signals categorized by significance (major, standard, brief), category (funding, M&A, product, compliance), and source type. It supports filtering and two view modes.

### Explainer Pages — Educational Layer
The "What Is an Expert Network?" page and buyer guides (consulting, PE, hedge funds) onboard users who are new to the category. These pages cover definitions, pricing, compliance, services, and provider selection.

### Trust Pages — Credibility Infrastructure
About, sources, verification, disclaimer, and privacy pages form the trust layer. They explain the research methodology, confidence labeling system, known limitations, and editorial independence.

## How Page Types Reinforce One Another

The pages are designed to cross-reference:

- **Directory → Profile:** Card clicks lead to deep-dive pages
- **Profile → Compare:** Provider pages link to the comparison tool with the provider pre-selected
- **Compare → Profile:** Comparison cells link back to provider profiles
- **Homepage → Compare:** Preset buttons jump directly into curated comparisons
- **Pricing → Profile:** Provider names in the pricing table link to profiles
- **News → Profile:** Each signal's related networks link to provider pages
- **Profile → News:** Provider pages show their most recent related signals
- **Explainer → Directory/Compare:** Educational pages guide readers toward the decision-support tools

This interconnection is not accidental. It reflects the understanding that buyers do not follow a single linear path — they loop between discovery, evaluation, and context-seeking.

## Navigation Architecture

### Primary Navigation
The header provides persistent access to: What's an Expert Network?, Networks, News, Compare, Pricing, and About.

### Buyer Pathways
The mobile drawer and homepage cards offer role-based and workflow-based entry points: Consulting Teams, PE & Hedge Funds, Enterprise Strategy, Transcript-Led, AI-Forward, and First-Time Buyer.

### Footer
The footer provides secondary navigation organized by purpose: Explore (directory, compare, pricing), Research Standards (about, sources, methodology, disclaimer), and Leading Profiles (top providers by name).

### Search Overlay
A global search overlay (triggered by `/` keyboard shortcut or icon) searches across all 33 providers with real-time filtering.

## Technical Architecture

### Static Generation
All pages are rendered at build time. The Astro framework processes JSON content files, applies templates, and outputs static HTML, CSS, and JavaScript. There are no API calls at runtime.

### Client-Side Interactivity
Three categories of client-side behavior:

1. **Compare tool controller** — manages provider selection, preset switching, diff mode, evidence notes, and URL state synchronization via a bundled TypeScript module
2. **Filtering and search** — directory filters, news filters, and the global search overlay run entirely in the browser
3. **Visual effects** — canvas-based particle animations, scroll-triggered fade-ins, and marquee animations with reduced-motion respect

### Content Validation
Build-time validation catches:
- Schema violations in provider and news JSON files (via Zod)
- Broken internal links across all 58 pages (via post-build link checker)
- TypeScript type errors (via `astro check`)

The full validation suite runs as `npm run verify`.

### URL State
The compare tool synchronizes its state to URL parameters (`?networks=glg,alphasights&preset=leaders`), making any comparison shareable via link. The news feed similarly persists filter state to the URL.
