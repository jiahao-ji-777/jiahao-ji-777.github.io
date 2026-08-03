# Jiahao Ji — Academic Homepage

A lightweight, dependency-free academic portfolio for <https://jiahao-ji-777.github.io/>.

## What is included

- Responsive single-page portfolio
- Light and dark themes
- Accessible keyboard navigation and reduced-motion support
- SEO metadata, sitemap, and robots file
- GitHub Actions deployment to GitHub Pages
- A durable design contract in [`DESIGN.md`](DESIGN.md)

## Preview locally

```bash
python3 -m http.server 8000
```

Open <http://localhost:8000>.

## Personalize before launch

Search `index.html` for `Jiahao Ji` and review:

1. Public name and title
2. Hero and About copy
3. Selected projects and ownership labels
4. Contact link (currently GitHub)
5. Optional affiliation, Google Scholar, ORCID, CV, and public email

The currently linked projects come from the public GitHub profile. Forked repositories are deliberately labeled as research explorations, not original projects.

## Publish

Create the public repository `jiahao-ji-777/jiahao-ji-777.github.io`, then run:

```bash
git push -u origin main
```

In the repository's **Settings → Pages**, set **Source** to **GitHub Actions**. The included workflow publishes on every push to `main`.

## Structure

```text
.
├── .github/workflows/pages.yml  # GitHub Pages deployment
├── DESIGN.md                    # Design and product source of truth
├── index.html                   # Content and semantic structure
├── styles.css                   # Visual system and responsive layout
├── script.js                    # Theme, reveal, and header behavior
├── favicon.svg
├── robots.txt
└── sitemap.xml
```
