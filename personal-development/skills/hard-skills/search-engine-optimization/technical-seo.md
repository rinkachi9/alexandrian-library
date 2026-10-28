# Technical SEO

## Summary

Technical SEO is the work that lets search engines crawl, render and index a site, and that makes pages fast, stable and usable on every device. It is invisible to most visitors, but when it fails, nothing else in SEO matters: a page that is blocked, broken, duplicated or never discovered cannot rank. Its core tasks are controlling crawling and indexing (robots.txt, noindex, canonical URLs, sitemaps), using correct HTTP status codes and redirects, making JavaScript content renderable, serving a good mobile experience, and meeting Google's Core Web Vitals for loading, responsiveness and visual stability.

## Prerequisites

[How search engines work](how-search-engines-work.md). Basic knowledge of how websites are served (URLs, HTML, HTTP) helps.

## Core concepts

### Definition

*Technical SEO* is the set of site-level and server-level optimizations that affect how search engines access, understand and evaluate a website, as opposed to the content of individual pages (on-page SEO) or signals from other sites (off-page SEO).

*Analogy.* Technical SEO is the plumbing and wiring of a house. Guests never admire the pipes, but if the water does not run or the lights flicker, nobody stays long, however beautiful the furniture. The analogy breaks because in a house a broken pipe is obvious, while a technical SEO problem can silently hide thousands of pages from search for months, which is why regular audits matter.

### Crawling control

- **robots.txt** is a text file at the site root that tells crawlers which paths they may not fetch. It controls crawling, not indexing: a blocked URL can still be indexed (without its content) if other pages link to it. Do not block CSS and JavaScript files that are needed to render pages.
- **XML sitemaps** list the URLs you want crawled, optionally with the date of last modification. Submit them in Google Search Console and reference them in robots.txt. Include only canonical, indexable URLs.
- **Internal linking** is the main way crawlers find pages. Pages with no internal links (*orphan pages*) are found late or not at all.
- **Crawl budget** matters mainly for very large sites. Wasting crawling on endless filter combinations, session IDs or duplicates slows the discovery of important pages (see [e-commerce SEO](e-commerce-seo.md#duplicate-urls-and-faceted-navigation)).

### Indexing control

- **noindex** (a robots meta tag or an `X-Robots-Tag` HTTP header) keeps a page out of the index. The page must be crawlable for the directive to be seen.
- **Canonical URL** (`<link rel="canonical" href="...">`) names the main version of a set of duplicate or near-duplicate URLs. Google treats it as a strong hint, alongside redirects, internal links and sitemaps.
- **Duplicates** arise from URL variants (with and without `www`, trailing slashes, parameters, upper and lower case), printer versions, and products in several categories. Pick one canonical form and make all signals point to it.

### HTTP status codes and redirects

| Code | Meaning | SEO use |
| --- | --- | --- |
| 200 | OK | Normal page |
| 301 | Moved permanently | Changed URLs, merged pages. Passes signals to the new URL |
| 302 or 307 | Moved temporarily | Short-term changes only |
| 404 | Not found | Removed pages with no replacement |
| 410 | Gone | Removed on purpose, may be dropped from the index faster |
| 5xx | Server error | Repeated errors reduce crawling and can drop pages from the index |

Avoid *redirect chains* (A to B to C) and *soft 404s* (a page that says "not found" but returns 200).

### JavaScript and rendering

Many sites build content with JavaScript in the browser. Google renders pages with a recent version of Chrome, but rendering can be delayed and can fail if scripts error, are blocked or depend on user interaction. Safer approaches for important content are *server-side rendering* or *static generation*, so the content is in the HTML response. Check with the URL Inspection tool in Search Console what Google actually sees.

### Mobile

Since July 2024 Google crawls and indexes all sites with its smartphone crawler (*mobile-first indexing*). The mobile version must have the same content, structured data and metadata as the desktop version. A responsive design (one HTML document that adapts to screen size) avoids differences between versions.

### Core Web Vitals

*Core Web Vitals* are Google's metrics of page experience, measured from real Chrome users (field data) at the 75th percentile of page loads:

| Metric | Measures | Good |
| --- | --- | --- |
| Largest Contentful Paint (LCP) | Loading: time until the largest visible element is rendered | 2.5 s or less |
| Interaction to Next Paint (INP) | Responsiveness: delay between user interactions and the next visual update | 200 ms or less |
| Cumulative Layout Shift (CLS) | Visual stability: unexpected movement of content | 0.1 or less |

INP replaced First Input Delay (FID) as a Core Web Vital on 12 March 2024. Page experience is one of many ranking signals. Good scores do not guarantee rankings, but very slow pages lose visitors (see [capturing attention](../content-marketing/capturing-attention.md#speed)).

Common fixes:

- LCP: compress and correctly size images, serve them in modern formats, preload the main image, reduce server response time, use a content delivery network.
- INP: reduce and split long JavaScript tasks, remove unnecessary third-party scripts.
- CLS: reserve space for images, ads and embeds with explicit dimensions, avoid inserting content above existing content.

### Security and international sites

- **HTTPS** is expected. Browsers mark plain HTTP pages as not secure.
- **hreflang** annotations tell search engines which language or regional version of a page to show to which users, for sites with several languages or countries.

### Technical audit

A periodic technical audit checks:

1. Index coverage in Search Console: pages indexed, excluded and why.
2. Crawl with a site crawler tool: status codes, redirect chains, broken links, orphan pages, duplicate titles, canonical tags.
3. Sitemaps: only canonical, indexable URLs.
4. robots.txt: nothing important blocked.
5. Rendering of key templates.
6. Core Web Vitals report in Search Console.
7. Mobile usability and structured data reports.

## Worked example

A shop moves from `http://shopname.com` to `https://www.shopname.com` and changes its category URL structure.

1. **Map old to new URLs** for every indexable page (2,400 rows in a spreadsheet).
2. **301 redirects** from each old URL directly to its new URL, no chains. Old URLs with no equivalent redirect to the closest category, or return 410 if nothing fits.
3. **Update internal links** to the new URLs so the site does not rely on redirects internally.
4. **Canonical tags** point to the new HTTPS URLs.
5. **New sitemap** with only new URLs, submitted in Search Console. Add the new domain property in Search Console.
6. **Monitor** for eight weeks: 404 errors, index coverage, impressions and rankings for the top 50 queries.

Common results of such migrations are a temporary dip in traffic while signals move. A migration done without redirects can lose most organic traffic. The URL count is invented for the example.

## Trade offs and when to use it

- **Platform defaults.** Hosted platforms handle many technical basics. You trade control for convenience, and some problems (duplicate URLs, slow apps) remain yours.
- **Speed versus features.** Every tracking script, chat widget and app slows the page. Decide which are worth their cost.
- **Perfect scores versus business value.** Fix problems that block indexing first. Chasing the last points of a speed score rarely pays off.
- **JavaScript frameworks** bring flexibility and rendering risk. Plan rendering before building.

## Common mistakes

- **Blocking with robots.txt to deindex.** Fix: use noindex on a crawlable page.
- **Redirecting everything to the home page.** Fix: redirect to the closest equivalent.
- **Canonical tags pointing to redirected or noindexed URLs.** Fix: point to the final, indexable URL.
- **Sitemaps full of non-canonical URLs.** Fix: generate them from canonical pages only.
- **Launching a redesign without a redirect map.** Fix: map every old URL first.

## Practice

1. Explain why a page blocked in robots.txt and marked noindex may stay in the index.
2. Name the three Core Web Vitals, what each measures and its "good" threshold.
3. What is a redirect chain, and why should you avoid it?
4. Run a free crawler on a small site and list the three most serious problems you find.

## Further reading

- Google Search Central. Introduction to robots.txt. [developers.google.com](https://developers.google.com/search/docs/crawling-indexing/robots/intro). What robots.txt does and does not do.
- Google Search Central. Consolidate duplicate URLs. [developers.google.com](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls). Canonicalization.
- Google Search Central. Understand the JavaScript SEO basics. [developers.google.com](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics). Rendering.
- web.dev. Web Vitals. [web.dev](https://web.dev/articles/vitals). Definitions and thresholds of the Core Web Vitals.
- web.dev (2024). Interaction to Next Paint becomes a Core Web Vital on March 12. [web.dev](https://web.dev/blog/inp-cwv-march-12). The change from FID to INP.
- Google Search Central Blog (2024). Mobile indexing vLast final final. [developers.google.com](https://developers.google.com/search/blog/2024/06/mobile-indexing-vlast-final-final.doc). The end of desktop crawling.

TODO: Confirm the Core Web Vitals thresholds and the 75th percentile rule on web.dev directly (not reachable from the working environment).
