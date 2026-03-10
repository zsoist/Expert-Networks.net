# Product Decisions

The reasoning behind the key design and editorial choices that shape ExpertNetworks.net.

---

## Why Compare-First UX

The comparison tool is the most complex and most valuable page on the site. This was a deliberate choice.

Most provider directories treat comparison as an afterthought — a checklist buried behind individual profiles. But for expert network buyers, the fundamental question is not "What does this provider offer?" but "How does this provider compare to my alternatives?"

By making the compare tool central — with 14 presets, diff mode, evidence notes, and shareable URL state — the site positions itself as a decision-support tool rather than just a directory.

## Why Public-Source Transparency

Every claim on the site is drawn from publicly available materials. This is a constraint, not an oversight.

The alternative — using private conversations, anonymous tips, or proprietary data — would make the content richer but harder to verify, harder to maintain, and harder to defend editorially. By committing to public sources, the site can be transparent about where its information comes from and honest about where it has gaps.

The confidence labeling system (verified, positioned, inferred, estimated) makes this transparency operational rather than theoretical.

## Why No Login, No Paywall

The site serves a professional audience that has limited patience for registration walls and upsell funnels. Gating the content behind a login would:

- Reduce the audience significantly
- Create friction at the moment of highest intent
- Undermine the independence positioning (a gated site looks like a lead-gen tool)

The decision to make everything publicly accessible without accounts reflects a belief that the value of the information is better served by reach than by capture.

## Why Multiple Page Types

A directory alone does not serve the full buyer journey. Different users arrive with different questions:

- **"What are expert networks?"** → Explainer page
- **"Who are the major providers?"** → Directory, Rankings
- **"How do GLG and AlphaSights compare?"** → VS page, Compare tool
- **"How much will this cost?"** → Pricing guide
- **"What's been happening in the industry?"** → News feed
- **"Which providers are best for PE workflows?"** → Buyer guide, Comparison preset

Each page type addresses a specific intent. Together, they cover the full range of questions a buyer might have across the evaluation process.

## Why Pricing Deserves Explicit Treatment

Expert network pricing is the most opaque aspect of the market. Most providers do not publish rates. Buyers often enter negotiations with no benchmark data.

A dedicated pricing guide — covering models, ranges, cost drivers, and provider-specific notes with confidence labels — fills a specific and valuable information gap. It also positions the site as the kind of resource that takes transparency seriously, even on sensitive commercial topics.

## Why Compliance and AI Deserve Explicit Treatment

These two dimensions are evolving rapidly and are high-stakes for buyers:

- **Compliance** matters because expert networks operate at the intersection of information access and securities regulation. Post-insider-trading-era buyers need to evaluate compliance postures carefully.
- **AI capabilities** matter because the market is shifting from concierge-model expert calls toward AI-assisted matching, synthesis, and transcript analysis. Buyers need to understand what's real versus what's marketing.

Both areas warranted structured treatment in provider profiles, comparison tables, and dedicated comparison dimensions.

## Why Trust and Usability Must Coexist

Professional audiences are skeptical by default. A site that claims to independently evaluate an industry but does not explain its methodology, disclose its limitations, or label its level of certainty will not be taken seriously.

The trust infrastructure (about, sources, methodology, disclaimer) is not an afterthought — it is integrated into the product:

- Confidence badges appear inline on provider profiles
- Disclaimers are woven into comparison and ranking pages
- The evidence framework is documented and linked from multiple entry points
- The site explicitly states what it does not know and what it cannot verify

This coexistence of usability and transparency is a core design principle.

## Why Buyer Pathways Are Valuable

Not all buyers enter through the same door. A PE associate evaluating compliance-first providers has different needs than a consulting team looking for fast-call platforms.

Buyer pathways — on the homepage, in the navigation drawer, and through comparison presets — route users to the most relevant starting point without requiring them to figure out the site's structure first.

## Why Structured Data Over Prose

Provider information is stored as structured JSON with Zod validation, not as free-form markdown. This choice has practical consequences:

- **Filterability:** Structured data enables the directory's multi-dimensional filtering
- **Comparability:** The compare tool depends on standardized fields across providers
- **Validation:** Zod schemas catch inconsistencies at build time
- **Maintainability:** Updating a provider's pricing model is a field change, not a paragraph rewrite

The tradeoff is that structured data requires upfront taxonomy design and ongoing schema maintenance. The benefit is that the data serves multiple page types simultaneously.

## Why Static Architecture

The site has no dynamic content that requires server-side rendering. Provider data changes on an editorial schedule, not in real time. All interactivity (compare tool, search, filters) runs in the browser.

A static architecture means:

- **Zero server costs** beyond CDN hosting
- **Zero runtime dependencies** to maintain or secure
- **Instant page loads** from global edge cache
- **Simplicity** — the build is the deployment

The main tradeoff is that content updates require a rebuild and redeploy. For a site updated weekly rather than hourly, this is acceptable.
