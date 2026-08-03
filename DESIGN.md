# Design

## Source of truth

- Status: Active
- Last refreshed: 2026-08-03
- Primary product surfaces: Single-page academic portfolio at `jiahao-ji-777.github.io`
- Evidence reviewed: User brief; public GitHub profile and repositories; live sites of Tanushree Banerjee, Yao-Chih Lee, Harry Ye, and Yash Belhe; no existing local site or design assets were present.

## Brand

- Personality: Curious, precise, grounded, youthful, technically confident.
- Trust signals: Clear project provenance, direct repository links, restrained claims, visible research themes.
- Avoid: Corporate template aesthetics, neon cyberpunk, dense CV walls, gratuitous gradients, fake metrics, or overstating forked work as original research.

## Product goals

- Goals: Establish a memorable academic identity; make research interests and selected work easy to scan; create a low-maintenance publishing base.
- Non-goals: Full publication database, long-form CMS, analytics, or a complex JavaScript application.
- Success signals: A visitor understands Jiahao's focus within 10 seconds and can reach relevant work or GitHub in one click.

## Personas and jobs

- Primary personas: Research peers, prospective collaborators, lab leads, and technically curious visitors.
- User jobs: Understand research direction, assess project fit, open technical work, and start a conversation.
- Key contexts of use: Desktop research browsing, mobile link sharing, and quick review from a CV or application.

## Information architecture

- Primary navigation: About, Work, Notes, Contact.
- Core routes/screens: One responsive page with anchored sections.
- Content hierarchy: Positioning statement → research identity → selected work → notes → contact.

## Design principles

- Editorial, not ornamental: Use typography, whitespace, and grid tension as the primary visual system.
- Evidence over performance: Every showcased item links to a public artifact and uses accurate ownership language.
- One vivid signal: Cobalt blue provides energy while the rest of the palette stays neutral.
- Tradeoffs: Static HTML keeps deployment and maintenance simple at the cost of automatic publication syncing.

### Reference audit

- Harry Ye: Borrow the thesis-like one-sentence hero and compact personal identity card; keep Jiahao's visual language more technical and less portfolio-like.
- Tanushree Banerjee: Borrow explicit research questions and clear project provenance; avoid dense text and tag accumulation.
- Yao-Chih Lee: Borrow the fast-scanning current-status signal and obvious academic utility links once CV/Scholar details exist; avoid employer-logo timelines until there is verified content.
- Yash Belhe: Borrow compact, contribution-first paper rows when publications exist; do not imitate the intentionally bare visual styling.
- Synthesis: Preserve the current editorial grid and cobalt signal color, add a research snapshot and recurring research questions, and leave academic links/publication rows contingent on real data.

## Visual language

- Color: Warm paper background, near-black text, cobalt accent, inverted dark theme.
- Typography: System sans for speed and clarity; restrained serif italics for a human editorial note.
- Spacing/layout rhythm: Generous section spacing, asymmetric two-column compositions, thin dividers.
- Shape/radius/elevation: Mostly square geometry; circular controls and orbital motifs; no drop shadows.
- Motion: Soft entrance reveals, subtle image scale, micro-interactions under 800ms.
- Imagery/iconography: Public GitHub avatar in monochrome; simple arrows and CSS orbital geometry.

## Components

- Existing components to reuse: None; greenfield static site.
- New/changed components: Fixed navigation, hero portrait, section label, interest list, project rows, note cards, contact panel, theme toggle.
- Variants and states: Featured/inverted project, regular project, enabled/coming-soon note, light/dark themes.
- Token/component ownership: CSS custom properties in `styles.css`; semantic content in `index.html`; behavior in `script.js`.

## Accessibility

- Target standard: WCAG 2.2 AA where practical.
- Keyboard/focus behavior: Visible focus rings, semantic links/buttons, skip link, anchor navigation.
- Contrast/readability: High-contrast neutral palette and large text; decorative color is never the only content cue.
- Screen-reader semantics: Landmark elements, heading order, descriptive labels, decorative visuals hidden.
- Reduced motion and sensory considerations: `prefers-reduced-motion` disables reveals, scrolling, and animations.

## Responsive behavior

- Supported breakpoints/devices: Modern evergreen browsers; compact phone through wide desktop.
- Layout adaptations: Two-column hero and sections collapse to one column below 900px; project actions reflow below 640px.
- Touch/hover differences: Core content does not depend on hover; tap targets are at least about 40px.

## Interaction states

- Loading: Core text and CSS render without JavaScript; remote avatar has intrinsic dimensions.
- Empty: Notes section includes an intentional "next up" state.
- Error: If the avatar fails, its frame remains a designed neutral surface.
- Success: Navigation scroll and contact links provide immediate feedback through native browser behavior.
- Disabled: Coming-soon note is a non-interactive article with reduced emphasis.
- Offline/slow network: All core assets are local except the GitHub avatar; no external fonts or frameworks.

## Content voice

- Tone: Direct, thoughtful, technically literate, optimistic without hype.
- Terminology: Prefer concrete research areas and verbs over vague claims like "passionate" or "cutting-edge."
- Microcopy rules: Short headings, sentence case, active voice, one clear action per component.

## Implementation constraints

- Framework/styling system: Dependency-free HTML, CSS, and JavaScript.
- Design-token constraints: Use existing custom properties before adding one-off values.
- Performance constraints: No client framework, external font, analytics, or heavy media.
- Compatibility constraints: GitHub Pages static hosting; no server-side functionality.
- Test/screenshot expectations: Validate HTML and links, load through a local HTTP server, inspect desktop and mobile screenshots.

## Open questions

- [ ] Confirm preferred public name and professional title / Jiahao / high impact on hero copy.
- [ ] Add current affiliation, education, and location if public / Jiahao / medium impact on credibility.
- [ ] Add a public email, Google Scholar, ORCID, and CV link / Jiahao / high impact on academic contact flow.
- [ ] Replace research-exploration repositories with original publications or projects as they become public / Jiahao / high impact on portfolio strength.
