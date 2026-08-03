# Jiahao Ji — Academic Homepage

A dependency-free academic homepage for <https://jiahao-ji-777.github.io/>.

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Content provenance

- Current role: user-confirmed full-time Algorithm Researcher at Noitom Robotics.
- Education, prior experience, honors, email, and Scholar URL: provided Chinese CV.
- Experience descriptions are intentionally limited to concise research keywords.
- Company wordmarks are stored locally; Noitom is sourced from its official site and ByteDance from the public-domain text-logo copy on Wikimedia Commons.
- CV source SHA256: `0d6e52bdb5d8ede746c78c114f0d61a9024df4766867a4057c631778df9439b1`.
- Phone number and other unnecessary personal details are intentionally excluded.
- Publications intentionally remain empty until the entries are explicitly approved for the public site.

## Files

```text
.
├── .github/workflows/pages.yml  # GitHub Pages deployment
├── DESIGN.md                    # Design and content contract
├── assets/                      # Local company wordmarks
├── index.html                   # Profile and academic content, including company wordmarks
├── styles.css                   # Responsive academic layout
├── script.js                    # Current footer year
├── favicon.svg
├── robots.txt
└── sitemap.xml
```

## Before the next content update

Confirm or add:

1. Professional portrait
2. Exact Noitom start month and public team name
3. Approved publication entries
4. Public CV, LinkedIn, and ORCID links

## Publish

Push `main`; the included GitHub Actions workflow deploys the static site to GitHub Pages.
