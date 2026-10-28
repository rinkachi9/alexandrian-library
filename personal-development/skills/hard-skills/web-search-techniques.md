# Web search techniques

## Summary

Web search techniques are ways to make a search engine return exactly what you need, and to judge whether what it returns is trustworthy. Search operators such as quotation marks, the minus sign and `site:` narrow results precisely, and image search finds where a picture came from. Finding a page is only half of research: studies of professional fact checkers show that the fastest way to judge an unfamiliar source is to leave it and read what other sites say about it, a method called lateral reading. Search engines change their features often, so some tricks in older guides no longer work.

## Prerequisites

None.

## Core concepts

### Definition

A *search operator* is a special character or word that changes how a search engine interprets a query, for example by requiring an exact phrase or limiting results to one website. *Search literacy* is the wider skill of choosing terms, refining queries and evaluating results.

*Analogy.* A plain query is like asking a librarian "something about jaguars". Operators are like adding "the animal, not the car, from the last five years, only from the zoo's website". The analogy breaks because a librarian understands why you ask, while a search engine applies operators literally and silently ignores some of them.

### Operators that work in Google

Google's help page "Refine Google searches" lists these operators. Put the operator directly against the term, with no space: `site:nytimes.com` works, `site: nytimes.com` does not.

| Operator | Effect | Example |
| --- | --- | --- |
| `"..."` | Exact phrase, words in the same order | `"how to fix a toaster"` |
| `-` | Exclude a word | `jaguar speed -car` |
| `site:` | Only results from one site or domain | `google site:time.com`, `vaccine site:gov` |
| `filetype:` | Only files of one type | `photoelectric effect filetype:pdf` |
| `before:` and `after:` | Pages by date, combinable into a range | `olympics after:2024-07-01 before:2024-08-15` |
| `*` inside quotes | A wildcard for one or more unknown words | `"* is thicker than water"` |
| `OR` | Either term | `marathon OR half-marathon training plan` |

The source notes use the misspelled example `"how fix toster"`. An exact phrase search with a typo returns only pages with the same typo, which shows why quotes should be used deliberately.

### Operators and features that changed

Search engines remove features without much notice. Examples:

- The `+` operator (force a word) was removed by Google in 2011, and the `~` synonym operator later. Use quotes around a single word to force it.
- The `cache:` operator stopped working in September 2024, after Google removed cached page links in early 2024. Google points to the Internet Archive's Wayback Machine through its "About this page" feature.
- The "Search tools" recipe filters described in the source notes (by ingredients, cooking time and calories) are no longer available in the same form.
- `define:` and comparisons such as `rice vs quinoa` still return a definition box or a comparison in many cases, but these are display features, not guaranteed operators.

Checked 2026-10 against Google's help page (through search summaries) and news reports of the changes.

### Image search

Reverse image search finds where an image appears online, older versions of it and similar images. In Google, the camera icon in the search bar (Google Lens) accepts an upload or an image URL. Other tools include Bing Visual Search and TinEye. It is useful for finding the origin of a photo, checking whether a "new" photo is old, and identifying a product from a picture.

### News archives

Google News Archive search, at `news.google.com/newspapers`, holds scanned historical newspapers. Google stopped adding newspapers to it in 2011, so coverage is fixed and uneven. The source notes claim that it reaches back to the mid-1880s. Reports from 2011 describe the archive as about 60 million pages covering about 250 years. For serious historical research, national libraries are usually better (for example the Library of Congress Chronicling America for US newspapers, or Polona of the National Library of Poland).

### Evaluating sources: lateral reading

*Vertical reading* means judging a website by reading it closely: its design, its "About" page, its logos and its references. *Lateral reading* means leaving the site soon after arriving and opening new tabs to find out what other, independent sources say about it.

In a study by Wineburg and McGrew (2019), 10 professional fact checkers, 10 PhD historians and 25 Stanford University undergraduates evaluated live websites on social and political topics. The fact checkers read laterally and reached better-supported conclusions in a fraction of the time. Historians and students mostly read vertically and were often misled by professional-looking design, official-sounding names and domains.

The *SIFT* method, developed by Mike Caulfield, turns lateral reading into four steps:

1. **Stop.** Before reading or sharing, ask whether you know the source.
2. **Investigate the source.** Search for who is behind it, outside the site itself.
3. **Find better coverage.** Look for trusted reporting or analysis on the same claim.
4. **Trace claims to the original.** Follow quotes, images and statistics back to where they first appeared.

### Search and AI answers

Search engines now often show AI-generated summaries above the results. A summary is a starting point, not a source: open the cited pages and check that they say what the summary claims. Summaries can merge sources, drop qualifications or be wrong.

## Worked example

Question: did a city really ban cars from its center in 2025, as a viral post claims?

1. **Precise search.** `"car ban" "city center" 2025 site:gov` finds nothing. The query is too narrow.
2. **Broaden and exclude noise.** `city center car ban 2025 -"black friday"` returns news articles from several outlets.
3. **Lateral reading.** The viral post links to a site called "Urban Mobility Today". A search for `"Urban Mobility Today"` (outside the site) shows it is run by an advocacy group. That does not make it wrong, but it means its framing should be checked.
4. **Trace the claim.** `site:` search on the city's official domain finds the council resolution. It restricts cars on six streets from 2026, not the whole center from 2025.
5. **Image check.** The photo in the post, searched with Google Lens, first appeared in 2019 in an article about another city.

Conclusion: the claim distorts a real but narrower decision and uses an unrelated photo. The city, sites and dates in this example are invented.

## Trade offs and when to use it

- **Operators save time** for precise questions. For exploratory questions, start broad and narrow down.
- **Over-narrow queries** can hide good results, as step 1 of the example shows.
- **Lateral reading takes a few minutes** and saves much more when a source is unfamiliar. For a well-known source on a routine question it is not needed.
- **Search engines personalize and localize results.** Two people can see different results for the same query.

## Common mistakes

- **Trusting a site because it looks professional.** Fix: read laterally.
- **Using quotes with typos or unusual word order.** Fix: quote only phrases you are sure of.
- **Relying on old operator lists.** Fix: check the search engine's current help page.
- **Treating an AI summary as the answer.** Fix: open and read the cited sources.

## Practice

1. Write a query that finds PDF reports about urban heat islands on government sites, published after 2023.
2. What is the difference between vertical and lateral reading, and which group in the Wineburg and McGrew study read laterally?
3. Name the four steps of SIFT.
4. Why does `"how fix toster"` return few or poor results?

Hints: question 1 combines `site:`, `filetype:` and `after:`.

## Further reading

- Google Search Help. Refine Google searches. [support.google.com](https://support.google.com/websearch/answer/2466433). The current list of supported operators.
- Wineburg, S., & McGrew, S. (2019). Lateral reading and the nature of expertise: Reading less and learning more when evaluating digital information. *Teachers College Record*, 121(11), 1-40. [doi:10.1177/016146811912101102](https://doi.org/10.1177/016146811912101102). The fact checker study.
- Caulfield, M. (2019). SIFT (The Four Moves). [hapgood.us](https://hapgood.us/2019/06/19/sift-the-four-moves/). The SIFT method.
- Schwartz, B. (2024). Google cache is dead. Search Engine Roundtable. [seroundtable.com](https://www.seroundtable.com/google-cache-dead-38112.html). The end of the cache operator.

TODO: Recheck the current behavior of `define:` and `vs` comparisons. Confirm the URL and date of Caulfield's SIFT post. Confirm the dates of removal of the `+` and `~` operators from a Google source.
