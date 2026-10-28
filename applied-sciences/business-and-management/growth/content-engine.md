# Content engine

## Summary

The content engine grows a business by building a large inventory of content that people find through search or share on social media. It comes in two forms: user-generated content, where users create pages that rank (reviews, salaries, pins), and editorial content, where the company writes guides and tools. It needs a large number of indexable pages and a category in which people search with clear intent before acting. It is slow to build and cheap to run, and its main risk is changes in search algorithms.

## Prerequisites

- [Growth engines](growth-engines.md)

## Core concepts

### Definition

The *content engine* turns content into a repeatable source of users: each page captures searches or shares, some visitors sign up, and in the user-generated form, new users create more pages. The economic condition is that the cost of creating and hosting content stays below the value of the traffic it brings. Search engine optimization is covered in [search engine optimization](../../../personal-development/skills/hard-skills/search-engine-optimization/README.md), and content marketing in [content marketing](../../../personal-development/skills/hard-skills/content-marketing/README.md).

### Analogy

A content engine is like a library that also attracts new authors: every book brings readers, some readers write new books, and the library grows by itself. An editorial engine is a library where the staff write all the books, which is slower. The analogy breaks because a search engine, not the library, decides which books are shown.

### Mechanism

**Two types.**

| Type | How pages are created | Examples |
| --- | --- | --- |
| User-generated content (UGC) | Users write reviews, post salaries, save pins; each item becomes an indexable page | Yelp, Glassdoor, TripAdvisor, Pinterest |
| Editorial or proprietary | The company produces guides, tools and data | NerdWallet's financial guides, HubSpot's blog |

**Requirements.** A large volume of indexable, useful pages, a category where people search with intent before acting ("best restaurants near me", "salary for nurse in Kraków"), and a way to convert visitors into users.

**The UGC loop.** Search visitor reads a page, signs up, contributes content, the new content ranks, more visitors arrive. This loop is what makes UGC a true engine; editorial content needs continuous paid or staff effort.

**Engine-product fit.** A product used before a search-driven decision (choosing a restaurant, comparing salaries) fits content well. A product people do not search for fits it poorly.

The user-generated content loop:

```mermaid
flowchart LR
  S[Search or social visitor] --> P[Reads a page]
  P --> U[Signs up]
  U --> C[Contributes content]
  C --> I[New indexable page]
  I --> S
```

## Worked example

A site where parents review nurseries in Polish cities starts with 300 editorial pages (one per district) and asks visitors to add reviews. After a year it has 9,000 reviews on 2,400 nursery pages. 70% of new users arrive from searches such as "nursery reviews + district name", and 4% of visitors write a review. The cost per page (moderation and hosting) is a fraction of the paid cost of the same visitors. The numbers are invented for the example.

## Trade offs and when to use it

Content compounds and is cheap per visitor once built, but it takes months, depends on search engines and social platforms that change their rules, and in 2025 to 2026 faces a new pressure: AI summaries on results pages reduce clicks to many sites (see [How search engines work](../../../personal-development/skills/hard-skills/search-engine-optimization/how-search-engines-work.md)). UGC needs moderation to stay trustworthy and legal.

## Common mistakes

- **Publishing thin or duplicated pages at scale.** Each page must answer a real search with useful content; search engines penalize scaled low-value pages.
- **Choosing content for a product nobody searches for.** Check search demand before committing.
- **Neglecting moderation of user content.** Plan moderation, verification and a process for removing illegal content.

## Practice

1. What is the difference between UGC and editorial content engines?
2. Why is UGC closer to a true engine than editorial content?

### Answers

1. In UGC users create the pages; in editorial the company creates them.
2. Because new users create new pages that bring more users, forming a loop without new company effort per page.

## Further reading

- Rachitsky, L. (2022). Step 6: Growth engines. Lenny's Newsletter. [Link](https://www.lennysnewsletter.com/p/growth-engines). Content as an engine.
- Balfour, B., Winters, C., Kwok, K. (2018). Growth loops are the new funnels. Reforge. [Link](https://www.reforge.com/blog/growth-loops). Content loops.
