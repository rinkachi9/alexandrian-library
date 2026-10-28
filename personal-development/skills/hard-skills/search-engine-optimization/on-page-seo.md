# On-page SEO

## Summary

On-page SEO is the optimization of what a single page contains and how it is marked up, so that search engines understand what the page is about and searchers choose it from the results. Its main elements are the content itself, the title, the meta description, headings, URLs, images with alt text, internal links and structured data. The single most important on-page factor is whether the content answers the query better than the alternatives. The other elements help the engine read the page and help the searcher click, but they cannot rescue a page that does not match the intent.

## Prerequisites

[How search engines work](how-search-engines-work.md) and [keyword research](keyword-research.md).

## Core concepts

### Definition

*On-page SEO* is the set of optimizations made within a page: its visible content and its HTML elements. It is distinct from *technical SEO* (site-wide conditions for crawling, indexing and speed, see [technical SEO](technical-seo.md)) and *off-page SEO* (signals from outside the site, mainly links, see [link building](link-building.md)).

*Analogy.* On-page SEO is like preparing a book for a library catalog. The title on the spine, the table of contents, the chapter headings, the captions and the cross-references let the librarian file it correctly and let readers see at a glance whether it answers their question. The analogy breaks because a librarian files a book once, while a search engine re-reads the page regularly and compares it, query by query, with thousands of competitors.

### Content: answering the query

- **Match intent.** Use the page type that the results show for the query (article, product page, category page, tool).
- **Answer early.** Put the direct answer or main benefit near the top, then expand.
- **Be complete for the intent.** Cover the sub-questions searchers have, which you find in "People also ask" and in customer questions.
- **Add original value.** First-hand experience, original photos, data, examples and expert input distinguish a page from the many that summarize the same sources. Google's guidance on helpful content asks whether a page offers original information or analysis beyond the obvious.
- **Keep it accurate and current.** Update facts, prices and dates.

### Title tag

The *title tag* (`<title>`) defines the page title. Search engines often use it as the clickable headline in results (Google calls this the *title link*).

- Describe the page's content specifically.
- Include the main query naturally, ideally near the start.
- Keep it short enough to display fully (often about 50 to 60 characters, but display is measured in pixels).
- Make each title unique on the site.

Since 2021 Google has generated title links from other page elements (such as the main heading) more often when it judges the title tag unhelpful, for example when it is too long, stuffed with keywords or the same on many pages.

### Meta description

The *meta description* is a short summary in the HTML head that search engines may show under the title. It does not directly affect ranking, but a clear, specific description can raise the share of searchers who click. Google often rewrites it with text from the page that better matches the query.

### Headings

One main heading (`<h1>`) that states the topic, and subheadings (`<h2>`, `<h3>`) that structure the content. Headings help readers scan (see [writing for the web](../copywriting/writing-for-the-web.md)) and help search engines understand the structure.

### URLs

Readable, descriptive URLs (`/guides/green-tea-bitter`) are easier to understand and share than parameter strings (`/p?id=8812`). Use hyphens between words, lowercase letters, and keep URLs stable: changing a URL requires a redirect.

### Images

- Descriptive file names (`sencha-leaves-brewed.jpg`).
- *Alt text* that describes the image accurately, which serves people using screen readers and helps image search. Do not stuff alt text with keywords.
- Compressed files in modern formats and correct dimensions, for speed.

### Internal links and anchor text

*Internal links* connect pages within the site. They help readers find related content, help crawlers discover pages and signal which pages are important. *Anchor text* is the clickable text of a link and tells readers and search engines what the target is about.

The source notes advise using the target keyword verbatim in anchor text. Descriptive anchor text is good practice, but using the identical exact phrase on every link looks unnatural. Describe the target page and vary the wording.

### Structured data

*Structured data* is machine-readable information, usually in JSON-LD format using the schema.org vocabulary, that describes the page's content: an article, a product with price and availability, a recipe, an event, an FAQ. It can make a page eligible for *rich results* (results with stars, prices, images). Structured data must describe what is visible on the page. For product data see [e-commerce SEO](e-commerce-seo.md#structured-data).

### What does not help

- The `meta keywords` tag is not used by Google.
- *Keyword stuffing* (repeating the query unnaturally) violates spam policies.
- Word count targets: there is no ideal length. Length should follow what the query needs.

## Worked example

Optimizing a guide targeting "why is my green tea bitter".

**Before:**

- Title: "Blog | TeaShop"
- URL: `/blog/post?id=341`
- H1: "Our thoughts on tea"
- First 300 words: the shop's history.
- One stock photo with alt text "tea tea green tea bitter tea buy tea".
- No internal links.

**After:**

- Title: "Why your green tea tastes bitter (and 3 ways to fix it)"
- Meta description: "Bitter green tea usually means water that is too hot or leaves steeped too long. Here are the temperatures and times that fix it."
- URL: `/guides/green-tea-bitter`
- H1: "Why green tea tastes bitter"
- Opening paragraph answers directly: water too hot, steeping too long, too many leaves.
- H2s: "Water temperature", "Steeping time", "Amount of leaves", "Tea quality", "Quick fix chart".
- Three original photos of the same tea brewed at 70 °C, 85 °C and 100 °C, with alt text such as "The same sencha brewed at 70, 85 and 100 degrees, the hottest brew is darkest".
- Internal links to the sencha category page ("loose leaf sencha") and to the brewing equipment guide.
- Article structured data with author and date.

The changes make the page match the informational intent, answer at once, add original value (comparison photos) and connect to related pages.

## Trade offs and when to use it

- **Quick wins.** Fixing titles, headings and internal links on existing pages is often the fastest SEO improvement.
- **Limits.** On-page optimization cannot make a page rank for a query it does not answer, or beat much stronger pages on its own.
- **Click versus ranking.** Titles and descriptions written only for clicks can disappoint readers. Promise what the page delivers.
- **Structured data effort.** Worth it for products, recipes, events and articles. Rich results are not guaranteed.

## Common mistakes

- **Same title on many pages.** Fix: unique, descriptive titles.
- **Burying the answer.** Fix: answer in the first paragraph.
- **Keyword-stuffed alt text and anchors.** Fix: describe images and targets naturally.
- **No internal links to new pages.** Fix: link from related pages and the relevant hub.
- **Structured data that does not match the page.** Fix: generate it from the visible content.

## Practice

1. List the on-page elements in this note and say which mainly affect ranking and which mainly affect clicks.
2. Rewrite the title, meta description and H1 of a page you know for a specific query.
3. Why might Google ignore your title tag and show another title?
4. Write alt text for three images on a product page.

## Further reading

- Google Search Central. SEO Starter Guide. [developers.google.com](https://developers.google.com/search/docs/fundamentals/seo-starter-guide). Titles, descriptions, headings, links and images.
- Google Search Central. Influencing your title links in search results. [developers.google.com](https://developers.google.com/search/docs/appearance/title-link). How Google generates title links.
- Google Search Central. Control your snippets in search results. [developers.google.com](https://developers.google.com/search/docs/appearance/snippet). Meta descriptions and snippets.
- Google Search Central. Introduction to structured data markup in Google Search. [developers.google.com](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data). Structured data and rich results.

TODO: Read the Google pages above directly (not reachable from the working environment) and confirm the 2021 change to title link generation.
