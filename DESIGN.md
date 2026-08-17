# Design

## Source of truth

- Status: Active
- Last refreshed: 2026-08-03
- Primary product surfaces: Single-page academic homepage at `jiahao-ji-777.github.io`
- Evidence reviewed: User feedback; public GitHub profile; Chinese CV `CV_Chinese (2).pdf`; live desktop/mobile references from `astrorix.github.io` and `tianxingchen.github.io` captured under `.omx/artifacts/visual-ralph/academic-homepage-reference/`.

## Brand

- Personality: Serious, clear, technically grounded, early-career, approachable.
- Trust signals: Current role, education, focused research descriptions, dated experience, direct academic links, and a source-backed publication entry.
- Avoid: Portfolio-style slogans, oversized typography, orbital graphics, decorative animations, dark mode, badge walls, inflated metrics, and unverified publication claims.

## Product goals

- Goals: Let research peers and hiring collaborators understand Jiahao's current role, background, and research focus quickly; provide an extensible publication-ready structure.
- Non-goals: Marketing site, personal blog, automatic publication sync, or complete CV replacement.
- Success signals: Current role and research topics are clear above the fold; visitors can find publications, experience, and education in one page, with direct profile links remaining above the fold.

## Personas and jobs

- Primary personas: Academic collaborators, research engineers, lab leads, and technical recruiters.
- User jobs: Identify Jiahao's research direction, scan research output and relevant experience, verify academic background, and use the profile links to make contact.
- Key contexts of use: Desktop research browsing, mobile sharing, CV/application links, and print/PDF capture.

## Information architecture

- Primary navigation: Publications, Experience, Education.
- Core routes/screens: One anchored page.
- Content hierarchy: Profile → News → Publications → Experience → Education.

## Design principles

- Academic first: Information density and provenance matter more than visual novelty.
- Quiet hierarchy: Typography, spacing, and thin rules organize the page without decorative UI.
- Honest incompleteness: Unavailable paper links remain visibly pending instead of pointing to an unverified destination.
- Tradeoffs: The site prioritizes clarity and maintainability over distinctive portfolio interactions.

## Visual language

- Color: White paper, very light gray page background, navy text, muted blue-gray secondary text, restrained academic blue links.
- Typography: Native/system sans-serif at conventional academic sizes.
- Spacing/layout rhythm: Centered 1000px page, generous but not theatrical section spacing, two-column section labels on desktop.
- Shape/radius/elevation: Flat white academic document, circular profile image, thin borders, no decorative shadow.
- Motion: Native anchor scrolling only; no entrance or decorative animation.
- Imagery/iconography: One profile image, restrained company wordmarks in Experience, a robot emoji favicon, and publication thumbnails only when real entries are added; no icon library.

## Components

- Existing components to reuse: Static HTML shell, deployment workflow, favicon, SEO files.
- New/changed components: Academic profile, compact navigation, news list, logo-supported chronology rows, keyword lists, and a figure-led publication entry.
- Variants and states: Desktop two-column and mobile single-column layouts; populated publication entries with an unavailable-paper state.
- Token/component ownership: CSS variables and component rules in `styles.css`; factual content in `index.html`.

## Accessibility

- Target standard: WCAG 2.2 AA where practical.
- Keyboard/focus behavior: Skip link, semantic anchors, visible focus outlines, no keyboard-only interactions.
- Contrast/readability: High contrast text, conventional body size, no color-only status encoding.
- Screen-reader semantics: Landmark elements, one H1, ordered headings, descriptive profile image alt text, valid time elements.
- Reduced motion and sensory considerations: No scripted motion or animation.

## Responsive behavior

- Supported breakpoints/devices: Modern evergreen browsers from 390px phone to wide desktop; print stylesheet included.
- Layout adaptations: Profile and section grids collapse below 760px; timelines collapse below 520px.
- Touch/hover differences: All core content is visible without hover; links remain native and easy to activate.

## Interaction states

- Loading: All content is serverless static HTML; only the GitHub profile image is an external visual request.
- Empty: Publications use a neutral, non-claiming empty state.
- Error: If the profile image fails, its dimensions remain reserved and text content is unaffected.
- Success: Native link and email behavior.
- Disabled: No disabled interactive elements.
- Offline/slow network: All core text, layout, and company wordmarks are local; the profile image may fail without affecting the page structure.

## Content voice

- Tone: Factual, concise, research-oriented, modest.
- Terminology: Use established technical terms from the source CV and current role update.
- Microcopy rules: No hype, emojis, vague superlatives, or fabricated metrics; dates and affiliations stay explicit.

## Implementation constraints

- Framework/styling system: Dependency-free HTML, CSS, and minimal JavaScript.
- Design-token constraints: Reuse the CSS custom properties at the top of `styles.css`.
- Performance constraints: No client framework, external font, large media, or runtime data fetching.
- Compatibility constraints: GitHub Pages static deployment; content must remain useful without JavaScript.
- Test/screenshot expectations: HTML validation, JS syntax check, link checks, Lighthouse, desktop 1440×1000 screenshot, mobile 390×844 screenshot, Visual Ralph verdict >= 90 against the approved synthesized reference direction.

## Open questions

- [ ] Replace the temporary GitHub avatar with a professional portrait / Jiahao / high visual impact.
- [ ] Confirm the exact Noitom full-time start month and whether `NR AI` should be public / Jiahao / medium content impact.
- [ ] Decide when to publish the two CV-listed papers / Jiahao / high academic impact.
- [ ] Add downloadable CV, LinkedIn, and ORCID URLs if available / Jiahao / medium contact impact.
