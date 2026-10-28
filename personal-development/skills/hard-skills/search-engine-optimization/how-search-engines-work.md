# How search engines work

## Summary

Search engine optimization (SEO) is the work of making pages easy for a search engine to find, understand and rank for the queries that matter to you, so that people reach them without paid ads. To do it well you need a correct model of the engine: it crawls the web to discover pages, renders and analyzes them, stores the useful ones in an index, and for every query ranks indexed pages using many signals about relevance, quality and usability. Each stage can fail for a different reason, and each part of SEO (technical, on-page, content, links) maps to one of the stages. Search results now also include AI-generated summaries, which change how much traffic a ranking brings.

## Prerequisites

None. This note is the entry point to [search engine optimization](README.md).

## Core concepts

### Definition of SEO

*Search engine optimization* is the practice of improving a website and its content so that it appears higher and more often in the unpaid (organic) results of search engines. The results page is called the *SERP* (search engine results page). SEO is distinct from search engine advertising (paid placements, often called SEA or PPC), although both compete for the same page and the same clicks.

*Analogy.* A search engine is a librarian in a library with billions of books and no fixed shelves. The librarian walks the corridors (crawling), reads each book that looks worth keeping and writes a catalog card (indexing), and, when a reader asks a question, hands over the books most likely to answer it (ranking). SEO is making your book easy to find in the corridors, giving it a clear title and contents, and earning recommendations from other trusted books. The analogy breaks because the real librarian is a set of algorithms that change several times a year, that nobody outside can fully inspect, and that increasingly answer the question itself instead of handing over a book.

### Stage 1: crawling

*Crawling* is the discovery and download of pages by automated programs called *crawlers* or *bots* (Google's is Googlebot). Crawlers find URLs by:

- following links from pages they already know,
- reading *XML sitemaps*, files that list URLs a site wants crawled,
- URLs submitted directly, for example in Google Search Console.

Crawling is limited. A *robots.txt* file at the root of a site tells crawlers which paths they may not fetch. Servers that respond slowly or with errors get crawled less. For very large sites, Google describes a *crawl budget*: the number of URLs it can and wants to crawl, which matters for sites with hundreds of thousands of URLs, such as large shops with filters (see [technical SEO](technical-seo.md)).

Since July 2024 Google crawls and indexes sites only with its smartphone crawler (*mobile-first indexing*), so the mobile version of a page is the version that counts.

### Stage 2: rendering and indexing

After downloading a page, the engine *renders* it (runs JavaScript to see the final content, like a browser), extracts text, links, images, metadata and structured data, and decides whether to store it in the *index*, its database of known pages.

Not every crawled page is indexed. Common reasons:

- the page carries a `noindex` directive,
- it is a duplicate or near duplicate of another page, and the engine chose another URL as *canonical* (the main version),
- it has little unique value,
- the content depends on JavaScript that failed to render,
- the server returned an error or a redirect.

### Stage 3: ranking and serving

For each query, the engine retrieves candidate pages from the index and orders them. Google states that its ranking systems consider, among others:

- **Meaning of the query.** What the person is looking for, including spelling corrections and synonyms.
- **Relevance.** Whether the page contains information that matches the query.
- **Quality.** Signals of expertise, authoritativeness and trustworthiness, including links from other sites.
- **Usability.** Page experience, such as working on mobile and loading reasonably fast.
- **Context.** The user's location, language and settings.

The exact signals and their weights are not public. Claims about "the 200 ranking factors" circulate widely but are not confirmed lists.

### Search features on the results page

The SERP is more than ten blue links. Depending on the query it may show: ads, an AI-generated summary (Google's *AI Overviews*), featured snippets, "People also ask" boxes, local results with a map, shopping results, images, videos and news. Each feature takes attention and clicks from the organic results below. In a 2025 Pew Research Center analysis of browsing data from 900 US adults, users clicked a traditional result link on 8% of visits to pages with an AI summary and on 15% of visits to pages without one.

### Quality guidelines and spam policies

Google describes its aim as rewarding "helpful, reliable, people-first content". Its *search quality rater guidelines*, used by human raters to evaluate results, describe *E-E-A-T*: experience, expertise, authoritativeness and trustworthiness. Google states that raters' assessments do not directly change rankings, but help it test ranking systems.

Google's *spam policies* list practices that can lower rankings or remove a site from results, including:

- keyword stuffing and hidden text,
- *cloaking* (showing search engines different content than users),
- *link schemes* (buying or selling links that pass ranking credit, excessive exchanges, large-scale guest posting with keyword-rich anchors),
- since March 2024: *scaled content abuse* (mass-produced pages made mainly to rank, by people or automation), *site reputation abuse* (low-quality third-party pages hosted on a strong site to borrow its ranking) and *expired domain abuse*.

### The parts of SEO mapped to the stages

| Stage | SEO discipline | Note |
| --- | --- | --- |
| Crawling and indexing | Technical SEO | [Technical SEO](technical-seo.md) |
| Understanding the page | On-page SEO, structured data | [On-page SEO](on-page-seo.md) |
| Matching queries | Keyword research, content | [Keyword research](keyword-research.md), [SEO content and blogging](seo-content-and-blogging.md) |
| Ranking signals of trust | Links, reputation | [Link building](link-building.md) |
| Online shops | All of the above for shop structures | [E-commerce SEO](e-commerce-seo.md) |
| Feedback loop | Measurement | [Measuring SEO](measuring-seo.md) |

### Beyond Google

Google has had a large majority of the global search market for many years, so most SEO advice targets it. Bing (which also supplies results to some other engines), regional engines such as Yandex, Baidu and Naver, marketplace search inside Amazon or Allegro, and search inside platforms such as YouTube follow similar principles with different details. Generative AI assistants that answer questions with citations are a growing, still unsettled channel.

## Worked example

Diagnosing why a new guide on a shop's blog gets no search traffic, stage by stage.

1. **Was it crawled?** In Google Search Console, the URL Inspection tool shows "Discovered, currently not indexed": Google knows the URL but has not indexed it. The page has no internal links except from the sitemap.
2. **Fix for discovery and priority.** Add links to the guide from the blog index, from two related articles and from the relevant category page.
3. **Was it indexed?** Two weeks later, the URL is indexed. The page now appears for the query in position 38.
4. **Why does it rank low?** The top results answer the question in the first paragraph and include original photos. The guide spends 300 words on the company history before answering. It also targets "tea brewing" (broad, informational) while the page is really about "green tea bitter".
5. **Fix for relevance and quality.** Move the answer to the top, add original photos of brewing at different temperatures, retitle around the specific query.
6. **Result to watch.** Impressions, clicks and average position in Search Console over the next two months.

The steps and numbers are invented to illustrate the diagnosis.

## Trade offs and when to use it

- **Slow and uncertain.** SEO results usually take months, and rankings change with algorithm updates outside your control.
- **Compounding.** Pages that rank bring visitors without a cost per click, often for years.
- **Competition.** Some queries are dominated by large brands. A new site should target specific, longer queries first.
- **Dependence.** A business with most traffic from one search engine is exposed to its changes, including AI summaries that answer without a click. Build owned channels too (see [email marketing](../content-marketing/email-marketing.md)).
- **Paid search** is fast and controllable, and stops when the budget stops. Many businesses use both.

## Common mistakes

- **Optimizing pages that are not indexed.** Fix: confirm indexing first.
- **Believing in fixed lists of ranking factors.** Fix: follow the engines' documented guidance and test.
- **Treating SEO as tricks.** Fix: most durable gains come from useful content, a sound site and genuine reputation. Tricks violate spam policies.
- **Ignoring the SERP.** Fix: look at what the results page actually shows for your query before deciding what to create.

## Practice

1. Describe the three stages of how a search engine works and one way each can fail.
2. Why can a URL blocked in robots.txt still appear in results?
3. Which three spam policies did Google add in March 2024?
4. Look at the SERP for a query in your field. List the features shown above the first organic result.

## Further reading

- Google Search Central. In-depth guide to how Google Search works. [developers.google.com](https://developers.google.com/search/docs/fundamentals/how-search-works). Crawling, indexing and serving.
- Google Search Central. SEO Starter Guide. [developers.google.com](https://developers.google.com/search/docs/fundamentals/seo-starter-guide). Google's introduction to SEO.
- Google Search Central. Spam policies for Google web search. [developers.google.com](https://developers.google.com/search/docs/essentials/spam-policies). Prohibited practices.
- Google Search Central. Creating helpful, reliable, people-first content. [developers.google.com](https://developers.google.com/search/docs/fundamentals/creating-helpful-content). Content quality and E-E-A-T.
- Google Search Central Blog (2024). Mobile indexing vLast final final (June 3, 2024). [developers.google.com](https://developers.google.com/search/blog/2024/06/mobile-indexing-vlast-final-final.doc). The completion of mobile-first indexing.
- Brin, S., & Page, L. (1998). The anatomy of a large-scale hypertextual Web search engine. *Computer Networks and ISDN Systems*, 30(1-7), 107-117. [doi:10.1016/S0169-7552(98)00110-X](https://doi.org/10.1016/S0169-7552(98)00110-X). The original description of Google.
- Pew Research Center (2025). Google users are less likely to click on links when an AI summary appears in the results. [pewresearch.org](https://www.pewresearch.org/short-reads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results/). AI summaries and clicks.

TODO: The Google Search Central pages could not be opened from the working environment. Read them and confirm the description of ranking systems and spam policies.
