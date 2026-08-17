# Design

## Source of truth

- Status: Active
- Last refreshed: 2026-08-17
- Primary product surfaces: Single-page academic homepage at `jiahao-ji-777.github.io`
- Evidence reviewed: User feedback; current implementation; viewport captures at 1440×900, 1366×768, 1024×768, 768×1024, and 390×844; public GitHub profile; Chinese CV `CV_Chinese (2).pdf`; academic-homepage references under `.omx/artifacts/visual-ralph/academic-homepage-reference/`.

## Brand

- Personality: Serious, clear, technically grounded, early-career, approachable.
- Trust signals: Current role, education, focused research descriptions, dated experience, direct academic links, and a source-backed publication entry.
- Avoid: Portfolio-style slogans, oversized typography, orbital graphics, decorative animations, dark mode, badge walls, stacked marketing cards, inflated metrics, and unverified publication claims.

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
- Desktop composure: Wide screens should use their space for readable proportions and stronger publication presentation, not larger empty margins.
- Tradeoffs: The site prioritizes clarity, scanability, and maintainability over distinctive portfolio interactions.

## Visual language

- Color: A restrained academic-blue scale: ink navy, medium blue links and kickers, pale blue-gray rules, a very light blue-gray page field, and white paper.
- Typography: Native/system sans-serif with compact heading line-height, a 65–75 character reading measure, and clearly separated metadata, title, authors, and body copy.
- Spacing/layout rhythm: Approximately 1120px usable desktop content, a 168px section rail with a 40px gap on wide screens, and denser vertical rhythm; the rail collapses before it can squeeze publication content.
- Shape/radius/elevation: White paper on a pale blue-gray desktop field, one subtle border and restrained shadow for the document shell, a lightly rounded 4:3 profile image, thin internal rules, and no stacked cards.
- Motion: Native anchor scrolling only; no entrance or decorative animation.
- Imagery/iconography: One full-color 4:3 profile image that preserves both subjects without cropping, restrained company wordmarks in Experience, a robot emoji favicon, and publication thumbnails only when real entries are added; no icon library.

## Components

- Existing components to reuse: Static HTML shell, deployment workflow, favicon, SEO files.
- New/changed components: Academic profile, compact navigation, stable desktop section rail, news list, logo-supported chronology rows, keyword lists, and a figure-led publication entry.
- Variants and states: Wide publication rows with a 320px-class figure, narrower two-column rows on tablet, single-column rows on mobile, and an unavailable-paper state.
- Token/component ownership: CSS variables and component rules in `styles.css`; factual content in `index.html`.

## Accessibility

- Target standard: WCAG 2.2 AA where practical.
- Keyboard/focus behavior: Skip link, semantic anchors, visible focus outlines, no keyboard-only interactions.
- Contrast/readability: High contrast text, conventional body size, no color-only status encoding.
- Screen-reader semantics: Landmark elements, one H1, ordered headings, descriptive profile image alt text, valid time elements.
- Reduced motion and sensory considerations: No scripted motion or animation.

## Responsive behavior

- Supported breakpoints/devices: Modern evergreen browsers from 390px phone to wide desktop; reference checks at 1440×900, 1366×768, 1024×768, 768×1024, and 390×844; print stylesheet included.
- Layout adaptations: The desktop paper shell flattens on tablet; the profile and publication grids collapse below 720px; timeline dates collapse below 560px.
- Touch/hover differences: All core content is visible without hover; links remain native and easy to activate.

## Interaction states

- Loading: All content and core visual assets are served locally as a static page.
- Empty: Future missing publications stay absent; the current unavailable paper URL is shown as non-interactive pending text.
- Error: If the profile image fails, its dimensions remain reserved and text content is unaffected.
- Success: Native link and email behavior.
- Disabled: No disabled interactive elements.
- Offline/slow network: All core text, layout, and visual assets are local; explicit image dimensions keep the layout stable during loading.

## Content voice

- Tone: Factual, concise, research-oriented, modest.
- Terminology: Use established technical terms from the source CV and current role update.
- Microcopy rules: No hype, emojis, vague superlatives, or fabricated metrics; dates and affiliations stay explicit.

## Implementation constraints

- Framework/styling system: Dependency-free HTML, CSS, and minimal JavaScript.
- Design-token constraints: Reuse the CSS custom properties at the top of `styles.css`.
- Performance constraints: No client framework, external font, large media, or runtime data fetching.
- Compatibility constraints: GitHub Pages static deployment; content must remain useful without JavaScript.
- Test/screenshot expectations: HTML validation, JS syntax check, link checks, overflow and broken-image assertions, screenshots at 1440×900, 1366×768, 1024×768, 768×1024, and 390×844, plus Lighthouse when available.

## Open questions

- [ ] Confirm the exact Noitom full-time start month and whether `NR AI` should be public / Jiahao / medium content impact.
- [ ] Decide when to publish the two CV-listed papers / Jiahao / high academic impact.
- [ ] Add downloadable CV, LinkedIn, and ORCID URLs if available / Jiahao / medium contact impact.
