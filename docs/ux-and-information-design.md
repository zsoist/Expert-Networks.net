# UX and Information Design

How the site's information architecture, navigation, and visual design serve its audience.

---

## Design for Professional Users

ExpertNetworks.net is designed for institutional buyers — consulting teams, PE professionals, corporate strategy groups — not casual consumers. This audience influences every design decision:

- **Information density over visual flair.** Pages present structured data in compact formats (tables, cards, badges) rather than sprawling marketing layouts.
- **Scan-first, read-second.** Section headers, badges, and visual hierarchies let users scan for relevance before committing to reading.
- **Minimal decoration.** The visual language is clean and restrained. Color is used functionally (category badges, confidence labels, provider gradients) rather than decoratively.
- **Professional tone.** Copy is precise and specific. No exclamation points, no urgency tactics, no conversion pressure.

## Homepage as Routing Layer

The homepage does not try to be everything. It presents six structured entry points (buyer pathways), surfaces the most important content (featured providers, current signals), and immediately establishes credibility (trust strip).

The routing logic:
- Users who know what they want → directory or compare tool
- Users who know their role → buyer pathway cards
- Users who are new to the category → explainer link
- Users who want to see what's current → news preview

## Multi-Page Content Strategy

The site uses a hub-and-spoke model:

```
                        Homepage (Hub)
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
   Discovery            Evaluation          Context
   (Directory)          (Compare)           (News)
        │                   │                   │
   Provider             VS Pages            Signal
   Profiles          Alt Pages              Detail
        │                   │
   Profile Detail     Presets/Filters
```

Each spoke serves a distinct purpose. The hub (homepage) routes users to the right spoke. Cross-links between spokes let users move laterally: from a provider profile to the comparison tool, from a news signal to the provider it mentions, from a pricing entry to the provider's profile.

## Trust Signposting

Trust indicators are distributed throughout the site, not concentrated on a single "About" page:

- **Homepage:** "No paid placements. No affiliations." appears above the fold.
- **Provider profiles:** Per-field confidence badges (verified/positioned/inferred/estimated) appear inline with data.
- **Compare tool:** Evidence notes toggle shows source confidence.
- **Pricing guide:** Each provider's pricing data includes a confidence label.
- **Footer:** Research standards links appear in a dedicated section.
- **Every page:** Sources and methodology are accessible from the global navigation.

This distributed approach works better than a centralized trust page because users encounter credibility signals at the moment they are evaluating information, not as a separate reading task.

## Information Density vs. Clarity

The site serves users who want depth and users who want quick answers. It handles this with progressive disclosure:

- **Cards** provide scan-level information (name, badges, one-line description)
- **Profile pages** provide structured detail (sections, accordions, timelines)
- **Confidence badges** add a meta-layer (how much should I trust this data point?)
- **Compare tool** provides relationship-level analysis (how do these providers differ?)

Users control their depth of engagement. A quick scanner can browse the directory, glance at badges, and leave with a shortlist. A thorough evaluator can read full profiles, toggle evidence notes, and build a custom comparison.

## Navigation Design

### Header
Fixed-position, 52px height. Contains: logo, primary navigation (5 links), search trigger, social link. Transitions from transparent to opaque as the user scrolls past hero sections.

### Mobile Drawer
Glass-morphism sidebar with expandable sections. Primary links, buyer pathways, and provider shortcuts all accessible from one panel. Drawer uses proper focus trapping and scroll lock.

### Search Overlay
Full-screen modal triggered by icon or `/` keyboard shortcut. Real-time search across all 33 providers with instant results. Keyboard accessible (Escape to close, Tab through results).

### Footer
Three-column layout organized by purpose: Explore, Research Standards, Leading Profiles. Includes quick-access links to the most common destinations.

## Accessibility

The site implements:

- **Keyboard navigation** throughout, with visible focus indicators
- **ARIA attributes** — `aria-expanded`, `aria-pressed`, `aria-hidden`, `aria-controls`, `aria-modal`, `aria-label` on interactive elements
- **Skip-to-main-content** link in the header
- **Reduced motion support** — particle animations, fade-ins, and marquee all respect `prefers-reduced-motion`
- **Touch targets** — minimum 44px on mobile interactive elements
- **Semantic HTML** — proper heading hierarchy, landmark regions, and form labels

## Visual Language

### Color System
- **Primary:** Near-black text (`#1D1D1F`) on off-white backgrounds (`#FBFBFD`)
- **Accent:** Apple-inspired blue (`#0071E3`) for interactive elements and CTAs
- **Provider gradients:** Each provider has custom gradient colors that appear on profile pages, cards, and badges
- **Confidence colors:** Green (verified), amber (inferred), blue (positioned), gray (not disclosed)

### Typography
Inter font family with system fallbacks. Sizes range from 10px (badges) to 36px+ (hero headings). Consistent weight hierarchy: extrabold for headings, semibold for section labels, medium for body text.

### Cards and Surfaces
Rounded cards (`16px` radius) with subtle borders and shadows. Hover states use elevated shadows and slight background shifts. No 3D effects, no gradients on surfaces.

### Dark Heroes
Key pages (homepage, compare, about, sources) use dark hero sections with particle canvas animations. These create visual weight and editorial gravitas at the top of important pages.
