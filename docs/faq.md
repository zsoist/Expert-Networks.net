# Frequently Asked Questions

Questions a recruiter, hiring manager, or visitor might ask about this project.

---

### Is this a commercial business or an independent project?

This is an independent project. It does not generate revenue, sell subscriptions, broker expert calls, or accept paid placements. It is a public-source research resource built and maintained by one person.

### Is the data public-source only?

Yes. All provider information is drawn from publicly available materials: provider websites, press releases, regulatory filings, industry reports, and trade press coverage. No information comes from private conversations, confidential sources, or insider access.

### What parts are editorial?

Rankings, comparisons, "Best For" assessments, and the "strengths and caveats" sections of provider profiles reflect editorial judgment. These are labeled as such and distinguished from factual claims (founding dates, certifications, headquarters) through the site's confidence labeling system.

### What makes this different from vendor directories?

Most provider directories in this space are either pay-to-play (providers pay for placement), maintained by providers themselves, or limited to basic listings. ExpertNetworks.net is:

- **Independent** — no provider has paid for coverage or positioning
- **Structured** — data is organized for comparison, not just listing
- **Transparent** — the methodology, confidence levels, and known limitations are documented
- **Comprehensive** — it covers pricing, compliance, AI, and market developments, not just service descriptions

### Why focus on expert networks?

The expert network industry is large (~$2B+), serves sophisticated institutional buyers, and has a significant public information gap. Most buyers evaluate providers through word of mouth, vendor marketing, and expensive gated reports. A free, structured, independent guide addresses a genuine need.

### What skills does this project demonstrate?

See the "What This Project Demonstrates" section in the [README](../README.md). In summary:

- Product strategy and market research
- Information architecture and taxonomy design
- Content system design (JSON schema, Zod validation, confidence labeling)
- Frontend development (Astro, Tailwind, TypeScript, client-side state management)
- Editorial discipline and trust-aware design
- SEO-conscious content structuring
- Independent end-to-end execution

### How should this repo be read if I'm evaluating the builder?

Recommended reading order:

1. **[README](../README.md)** — project overview and portfolio framing
2. **Visit the live site** — [expertnetworks.net](https://expertnetworks.net/) — try the comparison tool, browse the directory, read a provider profile
3. **[docs/project-story.md](project-story.md)** — origin, motivation, and scope evolution
4. **[docs/product-decisions.md](product-decisions.md)** — reasoning behind key design choices
5. **[docs/methodology-and-standards.md](methodology-and-standards.md)** — editorial rigor and confidence system
6. **[docs/page-guide.md](page-guide.md)** — detailed page-by-page documentation

### How many providers are tracked?

33 as of March 2026. The directory is a curated and expanding subset of the market, not a complete census.

### How is the information kept current?

Content is updated on an editorial schedule as new public information becomes available. The news feed tracks industry developments continuously. Provider profiles are updated when material changes (acquisitions, product launches, certifications, pricing changes) are identified through public sources.

### What technology is the site built with?

- **Framework:** Astro 5 (static site generator)
- **Styling:** Tailwind CSS with a custom design token system
- **Language:** TypeScript
- **Content:** JSON files validated by Zod schemas
- **Hosting:** Cloudflare Pages (static deployment)
- **Validation:** Build-time link checking (8,800+ references), TypeScript type checking, schema validation

### Is the source code available?

The source code lives in a private repository. This public repository contains the project documentation, editorial standards, and portfolio-oriented explanation of the work.

### Can I contribute corrections?

Yes. If you notice factual errors, outdated information, or broken functionality, please open an issue with the specific page URL and a public source supporting the correction. See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

### Is this site affiliated with any expert network provider?

No. The site has no affiliations, partnerships, referral arrangements, or sponsorship agreements with any provider listed on the site.
