# Link building

## Summary

Links from other websites are one of the oldest signals search engines use to judge which pages are trustworthy and important, going back to Google's PageRank in 1998. Link building is the work of earning such links: creating material others want to cite (original data, tools, expert guides), telling the right people about it, and getting mentioned in press and partner sites. Search engines prohibit manipulating this signal by buying links, exchanging them at scale or mass-producing guest posts with keyword-rich anchors, and paid links must be marked as such. Links matter less than relevance and content, but in competitive fields they often decide which of several good pages ranks first.

## Prerequisites

[How search engines work](how-search-engines-work.md) and [on-page SEO](on-page-seo.md) for anchor text.

## Core concepts

### Definition

A *backlink* (inbound link) is a link from another website to yours. *Link building* is the deliberate effort to increase the number and quality of backlinks. Related terms:

- *Anchor text*: the clickable text of the link.
- *Referring domain*: a distinct website linking to you. Ten links from one site count as one referring domain.
- *Link attributes*: `rel="nofollow"`, `rel="sponsored"` and `rel="ugc"` tell search engines about the nature of a link.

*Analogy.* Links work like citations in academic research. A paper cited by many respected papers in its field is probably important. A paper cited by a hundred unknown papers written by the same author is suspicious. The analogy holds for quality, relevance and independence of citations. It breaks because academic citations are rarely bought, while links have a market, so search engines must actively filter manipulated links.

### PageRank

Sergey Brin and Larry Page described *PageRank* in 1998: a page's importance is estimated from the number and importance of the pages linking to it, computed recursively, as if a "random surfer" clicked links forever and the score were the share of time spent on each page. A link from an important page passes more value than a link from an obscure one, and value is divided among a page's outgoing links. Google states that PageRank is still one of its signals, combined with many others, and the original formula has been refined over time.

### What makes a link valuable

- **Relevance:** a link from a site about tea is worth more to a tea shop than one from a site about car parts.
- **Authority and trust** of the linking site.
- **Editorial independence:** the linking site chose to link because the content is useful.
- **Placement:** links within the main content count more than links in footers or sidebars, by most practitioners' observation.
- **Traffic:** links that real people click bring visitors as well as ranking signals.

### Link attributes

In September 2019 Google introduced `rel="sponsored"` for paid or advertising links and `rel="ugc"` for user-generated content such as comments and forum posts, and began treating `nofollow` as a hint rather than a strict instruction. For crawling and indexing, the change took effect in March 2020. Paid links, including links in sponsored posts and affiliate links, must carry `sponsored` or `nofollow`.

### Link schemes

Google's spam policies prohibit *link schemes*, practices intended to manipulate ranking through links, including:

- buying or selling links that pass ranking credit, including exchanging goods or services for links,
- excessive link exchanges ("link to me and I will link to you"),
- large-scale article marketing or guest posting campaigns with keyword-rich anchor text,
- automated programs or services that create links,
- requiring a followed link as part of terms of service or a contract,
- *private blog networks*: sites created only to link to a target.

Consequences range from links being ignored to manual actions that lower a site's rankings.

### Ways to earn links

| Approach | How it works | Effort | Note |
| --- | --- | --- | --- |
| Original research and data | Publish a survey, a dataset or an analysis others cite | High | One of the most reliable ways to earn press links |
| Useful tools and resources | Calculators, templates, checklists | Medium to high | Earn links from guides and lists |
| Expert content | The best guide on a specific topic | Medium | Earns links slowly over time |
| Digital PR | Pitch a genuinely newsworthy story or expert comment to journalists | Medium | Responding to journalists' requests for expert sources is a common entry point |
| Guest articles | Write a useful article for another site's audience | Medium | Acceptable when the value is the article, not the link. Large-scale guest posting for links violates policies |
| Partnerships and suppliers | Partners, manufacturers and associations list you | Low | Often overlooked |
| Unlinked mentions | Ask sites that mention you without a link to add one | Low | Polite request, no payment |
| Broken link replacement | Find broken links on relevant pages and suggest your equivalent resource | Medium | Works when your resource is genuinely equivalent |

The source notes mention guest posts and press mentions as the two main methods, and suggest analyzing backlinks with tools such as Ahrefs to find sites in your niche that accept guest posts. The source also mentions a "simple growth hack" for press mentions without describing it.

### Outreach

*Outreach* is contacting site owners or journalists about your content. Good outreach is short, specific and useful to the recipient: why this content helps their readers, not why you want a link. Personal data rules apply to outreach emails (see [outreach and prospecting](../client-acquisition/outreach-and-prospecting.md#law-and-consent)).

## Worked example

A tea shop wants links to its brewing guides.

1. **Asset.** The shop brews 12 green teas at four temperatures, has five people blind-taste them, and publishes "The bitterness map of green tea" with a chart, method and raw data.
2. **Targets.** 30 relevant sites: tea blogs, coffee and tea magazines, cooking sites that wrote about tea in the last year, and two journalists who cover food.
3. **Pitch** (example):

> Subject: Data for your green tea article
>
> Hello Ewa, your article on morning teas mentions bitterness. We tested 12 green teas at four temperatures with a blind panel. Sencha brewed at 100 °C was rated twice as bitter as at 75 °C. The chart and full data are free to use with credit: [link]. Happy to send the raw spreadsheet.

4. **Results after three months (invented).** 6 links from relevant sites, one mention in a food magazine, and the guide moves from position 14 to position 6 for its main query, alongside on-page improvements made at the same time, so the effect of the links alone is uncertain.

The panel of five people is too small for strong claims, and the published method says so.

## Trade offs and when to use it

- **Earned links take time and assets.** There are no fast, safe shortcuts.
- **Buying links** may work briefly and risks penalties and wasted money. It also violates search engine policies.
- **Links versus content.** Without good content, links do not stay. With excellent content in an uncompetitive niche, few links may be needed.
- **Measuring impact is hard,** because rankings change for many reasons at once.

## Common mistakes

- **Chasing link counts.** Fix: aim for relevant, editorial links.
- **Keyword-rich anchors everywhere.** Fix: let linking sites choose natural anchors.
- **Mass guest posting.** Fix: write a few genuinely useful guest articles for relevant audiences.
- **Unmarked paid links.** Fix: mark sponsored links with `sponsored` or `nofollow`.
- **Pitches about yourself.** Fix: pitch what the recipient's readers gain.

## Practice

1. Explain PageRank in two sentences using the random surfer idea.
2. Which link attributes did Google introduce in 2019, and when should each be used?
3. List four practices Google's spam policies classify as link schemes.
4. Design a linkable asset for a business you know and list ten sites that might link to it.

## Further reading

- Brin, S., & Page, L. (1998). The anatomy of a large-scale hypertextual Web search engine. *Computer Networks and ISDN Systems*, 30(1-7), 107-117. [doi:10.1016/S0169-7552(98)00110-X](https://doi.org/10.1016/S0169-7552(98)00110-X). PageRank.
- Google Search Central. Spam policies for Google web search: link spam. [developers.google.com](https://developers.google.com/search/docs/essentials/spam-policies#link-spam). Prohibited link practices.
- Google Search Central. Qualify your outbound links to Google. [developers.google.com](https://developers.google.com/search/docs/crawling-indexing/qualify-outbound-links). The nofollow, sponsored and ugc attributes.
- Google Search Central Blog (2019). Evolving "nofollow": new ways to identify the nature of links. [developers.google.com](https://developers.google.com/search/blog/2019/09/evolving-nofollow-new-ways-to-identify). The 2019 change.

TODO: Verify the URL of the 2019 Google blog post and the statement that PageRank remains a current signal, against Google's documentation.
