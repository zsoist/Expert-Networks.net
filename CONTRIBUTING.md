# Contributing to ExpertNetworks.net

Thank you for your interest in this project.

ExpertNetworks.net is an independent research platform. While the site is publicly accessible, contributions to content and code follow specific editorial and technical standards.

## How to Contribute

### Reporting Issues

If you notice factual errors, broken links, outdated provider information, or UX issues on the live site:

1. Open an issue using the appropriate template (bug report, documentation, or feature request).
2. Include the specific page URL and a clear description of the issue.
3. For factual corrections, include a public source supporting the correction.

### Suggesting Improvements

Feature suggestions, UX feedback, and content coverage ideas are welcome. Please open a feature request issue with:

- A clear description of the improvement
- The user problem it would address
- Any relevant examples or references

### Content Standards

All content on ExpertNetworks.net follows these editorial standards:

- **Public-source only.** All provider information must be traceable to publicly available materials.
- **Confidence labeling.** Claims are tagged as verified, positioned, inferred, or estimated. New content must follow this convention.
- **No promotional framing.** The site does not accept paid placements, sponsored content, or affiliate arrangements.
- **Careful language.** Rankings and comparisons are framed as editorial interpretation, not objective truth.

### Technical Standards

- The site is built with Astro (static output), Tailwind CSS, and TypeScript.
- Content is stored as JSON files validated by Zod schemas.
- All changes must pass `npm run verify` (build + link validation + type checking).
- Provider slugs must remain consistent across network files, news references, and comparison presets.

## Code of Conduct

Be respectful, constructive, and specific. This is a small, focused project. Contributions that align with the site's editorial mission and technical standards are most likely to be accepted.

## Questions

If you're unsure whether a contribution fits, open a discussion issue first. Context about the project's goals and constraints can be found in the [`docs/`](docs/) folder.
