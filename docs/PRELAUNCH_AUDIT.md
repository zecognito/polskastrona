# PolskaStrona.com — pre-launch audit

Audit date: 2026-09-22

Branch: `development`

Production status: not merged, deployed, or published

## Scope

- 30 launch articles (001–030)
- 6 category hubs
- Homepage and custom 404 page
- Shared navigation, responsive styles, and mobile menu behavior
- Metadata, canonical URLs, crawl controls, and sitemap

## Result

Status: **pre-launch candidate ready for owner review**

The approved full homepage design was restored after the initial staging build
was found to contain a reduced placeholder shell. The restored homepage keeps
the approved visual system, full search hero, eight topic cards, three guided
journeys, five popular guides, and state-information panel.

- 38 HTML pages parsed successfully
- Exactly 30 article pages detected
- 38 unique canonical URLs
- 0 unresolved internal links
- 0 broken in-page anchors
- 0 duplicate element IDs
- 0 missing titles, descriptions, canonicals, or H1 headings
- 0 missing article-template components (`Krótka odpowiedź`, `W skrócie`, TOC, `Sprawdzono`, related links, sources)
- 0 JavaScript syntax errors
- 0 CSS brace-balance errors
- 0 whitespace errors from `git diff --check`
- Homepage search routes the current launch topics to the matching guide
- Homepage navigation, topic cards, journeys, and popular guides point to valid launch URLs

## Preservation checks

The editorial `<main>` content of Articles 001–007 matches the pre-existing `development` branch. Their changes are limited to shared navigation, metadata, canonical/SEO tags, and the common mobile-menu script.

Articles 008–030 were staged from their approved artifacts into the URL paths defined by `docs/LAUNCH_MAP.md`. Their approved editorial bodies were preserved while inline preview CSS was replaced with the shared production stylesheet.

## Launch architecture

- `/pieniadze/` — Articles 001–008
- `/dom/` — Articles 009–014
- `/samochod/` — Articles 015–021
- `/praca/` and `/podatki/` — Articles 022–025
- `/emerytura/` — Articles 026–030

## SEO and crawl readiness

- Self-referencing absolute canonical on every HTML page
- Unique title, meta description, and canonical per page
- Open Graph and Twitter summary metadata
- Polish language declaration (`lang="pl"`)
- Article structured data on Articles 008–030
- Website structured data on the homepage
- `robots.txt` points to `sitemap.xml`
- Sitemap contains all 37 indexable launch URLs and excludes the 404 page
- Custom 404 page uses `noindex,follow`

## Mobile and navigation readiness

- Article 007's compact mobile typography is the shared baseline for all 30 articles
- Article layout collapses to one column below 900 px
- Related cards collapse to one column on phones
- Tables use the compact phone scale
- Mobile navigation opens from an accessible button, updates `aria-expanded`, closes after selection, and closes with Escape
- All five live launch categories are reachable from the global navigation
- Unbuilt future categories were removed from the launch homepage so they do not create dead routes

## Deliberately not performed

- No merge to `main`
- No deployment or publication
- No production-domain changes
