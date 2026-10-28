# SEO fundamentals

## Summary

Search engine optimization (SEO) is the work of making pages easy for a search engine to find, understand and rank for the queries that matter to you, so that people reach them without paid ads. A search engine works in three stages: it crawls the web, indexes what it finds and ranks indexed pages for each query. SEO therefore has three parts: technical work so that pages can be crawled and indexed, content that answers what people search for, and links and reputation that signal trust. Shortcuts that try to trick the ranking, such as bought links or keyword stuffing, break Google's spam policies and can remove a site from results.

## Prerequisites

None. [Content marketing](../content-marketing/content-marketing.md) explains why organic traffic is valuable.

## Core concepts

### Definition

*Search engine optimization* is the practice of improving a website and its content so that it appears higher and more often in the unpaid (organic) results of search engines. The results page is called the *SERP* (search engine results page). SEO is distinct from search engine advertising (paid placements), although both target the same results page.

*Analogy.* A search engine is a librarian in a library with billions of books and no fixed shelves. The librarian walks the corridors (crawling), writes a catalog card for each book worth keeping (indexing) and, when a reader asks a question, hands over the books most likely to answer it (ranking). SEO is making your book easy to find in the corridors, giving it a clear title and table of contents, and earning recommendations from other trusted books. The analogy breaks because the real librarian is a set of algorithms that change several times a year and that no outsider can inspect.

### How a search engine works

1. **Crawling.** Programs called *crawlers* (Google's is Googlebot) follow links and read sitemaps to discover URLs and download pages. A *robots.txt* file tells crawlers which paths they may not fetch. It controls crawling, not indexing: a blocked URL can still be indexed if other sites link to it.
2. **Indexing.** The engine renders the page, extracts its text, links, images and structured data, and stores it in the *index*, the engine's database of known pages. Not every crawled page is indexed. Duplicate or low value pages are often left out.
3. **Ranking (serving).** For each query the engine selects and orders indexed pages by many signals: relevance to the query, quality and reliability of the content, usability of the page, the user's location and language, and links from other sites.

### Keyword research

A *keyword* is a word or phrase people type into a search engine. *Keyword research* finds the queries your audience uses and decides which ones to target. Four factors matter:

| Factor | Question | Source of data |
| --- | --- | --- |
| Volume | How many people search for it per month? | Google Keyword Planner, commercial tools such as Ahrefs or Semrush |
| Competition | How hard is it to rank? Tools show an estimated *keyword difficulty* | Commercial SEO tools, a look at the current top results |
| Relevance | Would your page genuinely satisfy this query? | Your own judgment |
| Intent | What does the searcher want to do: learn, compare, buy, or find a specific site? | The query wording and the current top results |

*Search intent* is the goal behind the query. "Ball gown wedding dresses" shows intent to buy a specific style. "Work dresses" is a different audience entirely for a bridal shop. Pages that do not match the intent rarely rank, however well written they are.

Free sources of keyword ideas:

- **Autocomplete.** Start typing a seed keyword in Google or Amazon and read the suggestions. Amazon's suggestions are product oriented and often contain attributes such as size or price.
- **Related searches and "People also ask"** on the Google results page.
- **Google Trends** for the direction of interest over time (see [product validation](../e-commerce/product-validation.md#search-and-trend-data)).

### Related terms and the LSI myth

The source notes recommend "LSI keywords". *Latent semantic indexing* (LSI) is an information retrieval method from the late 1980s. Google's John Mueller stated in 2019 that there is no such thing as LSI keywords in Google's ranking. The useful part of the advice remains: a thorough page naturally uses related terms, attributes and questions that searchers care about. For a blender, terms such as "14 speeds", "450 W" and "1.4 l glass jar" that appear in many product listings show what buyers compare. Use them because they describe the product, not to satisfy a supposed algorithm.

### Site architecture

*Site architecture* is how pages are organized and linked. A good structure helps visitors and crawlers alike:

- a simple hierarchy (home, categories, subcategories, items) that can grow without being rebuilt,
- every important page reachable in a few clicks from the home page,
- menus and internal links that use descriptive text,
- one URL per piece of content.

### Indexing control

- **noindex.** A `noindex` robots meta tag or HTTP header tells search engines not to show a page in results. Use it for pages with no search value, such as internal search results or thin tag pages. The page must not be blocked in robots.txt, or the crawler never sees the tag.
- **Canonical URL.** A `rel="canonical"` link tells search engines which URL is the main version of a set of duplicates, for example a product reachable under several category paths or with tracking parameters. Without it the engine may pick the wrong version, split ranking signals between duplicates or spend crawling on copies instead of unique pages. Google treats the canonical tag as a strong hint, not a command.
- **Better content.** Sometimes the right fix for near-duplicate pages is to make them genuinely different and useful instead of hiding them.

### Technical SEO

*Technical SEO* covers everything that lets search engines crawl, render and index a site, and that makes the page fast and usable:

- an XML *sitemap* listing important URLs, submitted in Google Search Console,
- a correct robots.txt,
- logical internal linking through menus and in-text links,
- pages that work on mobile, since Google uses the mobile version of a page for indexing,
- compressed, correctly sized images,
- HTTPS,
- *Core Web Vitals*, Google's page experience metrics: Largest Contentful Paint (LCP, loading; good at 2.5 s or less), Interaction to Next Paint (INP, responsiveness; good at 200 ms or less) and Cumulative Layout Shift (CLS, visual stability; good at 0.1 or less). INP replaced First Input Delay (FID) as a Core Web Vital on 12 March 2024.

### On-page SEO

*On-page SEO* is the optimization of the visible content and the HTML of a page:

- **Title tag.** The clickable title in search results. It should describe the page and contain the main keyword naturally.
- **Meta description.** A short summary that search engines may show under the title. It does not directly affect ranking, but it affects whether people click. Google often rewrites it.
- **Headings** that structure the content.
- **Image alt text** that describes the image accurately, for accessibility and image search.
- **Descriptive file names and URLs** (`/blenders/glass-jar-blender-450w` rather than `/p?id=8812`).
- **Content that answers the query** better than the alternatives.

The `meta keywords` tag is not used by Google for ranking.

### Content quality

Google describes its goal as rewarding "helpful, reliable, people-first content". Its search quality rater guidelines use the concept *E-E-A-T*: experience, expertise, authoritativeness and trustworthiness. Raters evaluate results to help Google test its ranking systems. Google states that the ratings themselves do not directly affect ranking. In practice, content that shows first-hand experience, cites sources and is maintained tends to do well over time.

### Links

*PageRank*, described by Brin and Page in 1998, ranked pages partly by the number and quality of links pointing to them, treating a link as a vote of confidence. Links from relevant, trusted sites still matter. Ways to earn them include original research and data, useful tools, press coverage and guest articles that are genuinely useful to the host site's readers.

Google's spam policies prohibit *link schemes*: buying or selling links that pass ranking credit, excessive link exchanges, large-scale guest posting or article campaigns with keyword-rich anchor text, and automated link creation. Paid or sponsored links must be marked with `rel="sponsored"` or `rel="nofollow"`. Since March 2024 the policies also cover *scaled content abuse* (mass-produced pages made mainly to rank, whether by people or automation), *site reputation abuse* (third-party pages placed on a strong site to borrow its ranking) and *expired domain abuse*.

### Internal links and anchor text

*Anchor text* is the clickable text of a link. Internal links help readers find related pages and help crawlers understand the structure. The source advises using the target keyword verbatim in anchor text. Descriptive anchor text is good practice, but repeating the identical exact-match phrase everywhere looks unnatural. Vary the wording and describe the target page.

### Blogging

A blog is a common way to target informational queries. Each post should target a specific query, be optimized like any other page, and, where it fits, link to the products that solve the problem it discusses. Posts can build credibility and attract links that help the whole site.

### Search with AI summaries

Google shows AI-generated summaries (AI Overviews) above many results. In a 2025 Pew Research Center analysis, users clicked a traditional result link on 8% of visits to pages with such a summary and on 15% of visits without one. Pages that only repeat widely available answers are most affected. Original data, first-hand experience, tools and commercial pages that answer a specific buying need are less easily replaced by a summary. This is a fast-moving area, checked 2026-10.

## Worked example

A small shop sells stainless steel water bottles and wants to rank for "insulated water bottle for kids".

1. **Intent.** The current top results are product category pages and comparison articles. The intent is commercial: parents comparing products.
2. **Page.** The shop creates a category page `/kids-water-bottles/` with a title tag "Insulated water bottles for kids (350 to 500 ml) | ShopName", a 150 word introduction answering what parents ask (leak-proof lids, dishwasher safety, how long drinks stay cold) and a filterable list of products.
3. **Duplicates.** The same products also appear under `/sale/` and with tracking parameters. Product pages get a canonical URL to their main path.
4. **Technical.** Product photos are compressed from about 2 MB to about 150 KB each. LCP on a mobile test improves from 4.1 s to 2.2 s.
5. **Internal links.** A blog post "How to clean a kids' water bottle" links to the category page with the anchor text "insulated bottles for kids".
6. **Links.** The shop publishes a small original survey of 300 parents about school drinking habits and offers it to parenting blogs. Two blogs cite it with a link.
7. **Measurement.** In Search Console the shop watches impressions, clicks and average position for the query over three months.

All numbers are invented for illustration.

## Trade offs and when to use it

- **Slow and uncertain.** Results usually take months, and ranking changes with algorithm updates outside your control.
- **Compounding.** Pages that rank bring visitors without a cost per click.
- **Competition.** Highly competitive queries may be out of reach for a new site. Target specific, longer queries first.
- **Dependence.** A business that relies on one search engine for most of its traffic is exposed to that engine's changes. Build owned channels too.
- **Paid search** is faster and fully controllable but stops when the budget stops.

## Common mistakes

- **Targeting volume without intent.** Fix: check the current top results before choosing a keyword.
- **Blocking a page in robots.txt and expecting it to disappear from results.** Fix: use `noindex` and let the page be crawled.
- **Duplicate pages without canonicals.** Fix: one main URL per content item.
- **Buying links or mass-producing pages.** Fix: earn links with content worth citing. These shortcuts violate spam policies.
- **Writing for algorithms instead of readers.** Fix: answer the query better than anyone else.

## Practice

1. Name the three stages of how a search engine works and one SEO task that belongs to each.
2. What is the difference between `noindex` and a robots.txt disallow rule?
3. Why is "LSI keywords" a misleading name, and what is the useful idea behind it?
4. Which metric replaced FID as a Core Web Vital, and when?
5. Choose a query relevant to a project of yours, look at the top five results and describe the search intent.

## Further reading

- Google Search Central. SEO Starter Guide. [developers.google.com](https://developers.google.com/search/docs/fundamentals/seo-starter-guide). Google's own introduction.
- Google Search Central. In-depth guide to how Google Search works. [developers.google.com](https://developers.google.com/search/docs/fundamentals/how-search-works). Crawling, indexing and serving.
- Google Search Central. Spam policies for Google web search. [developers.google.com](https://developers.google.com/search/docs/essentials/spam-policies). Link schemes, scaled content abuse and other prohibited practices.
- Google Search Central. Creating helpful, reliable, people-first content. [developers.google.com](https://developers.google.com/search/docs/fundamentals/creating-helpful-content). Google's guidance on content quality and E-E-A-T.
- web.dev (Google Chrome team). Interaction to Next Paint becomes a Core Web Vital on March 12. [web.dev](https://web.dev/blog/inp-cwv-march-12). The change from FID to INP.
- Brin, S., & Page, L. (1998). The anatomy of a large-scale hypertextual Web search engine. *Computer Networks and ISDN Systems*, 30(1-7), 107-117. [doi:10.1016/S0169-7552(98)00110-X](https://doi.org/10.1016/S0169-7552(98)00110-X). The original description of Google and PageRank.
- Schwartz, B. (2019). Google: There is no such thing as LSI keywords. Search Engine Roundtable. [seroundtable.com](https://www.seroundtable.com/google-lsi-keywords-27970.html). The report of John Mueller's statement.

TODO: The Google Search Central pages could not be opened from the working environment (network policy). Their content here comes from search summaries and prior knowledge. Read them and confirm the Core Web Vitals thresholds and the current wording of the spam policies.
