# Paid social advertising

## Summary

Paid social advertising means buying placements on social platforms, such as Meta (Facebook and Instagram), TikTok, LinkedIn and Pinterest, to show ads to chosen audiences and optimize for an objective such as purchases or leads. Platforms run auctions and use machine learning to find the people most likely to take the action you pay for, so the advertiser's main levers are the objective, the creative, the offer, the budget and the measurement setup. Since Apple's App Tracking Transparency in 2021, tracking is less complete and results rely more on server-side data and modeling. Testing whether a product sells with ads, as the source notes describe for dropshipping and private label, works only with a clear break-even calculation and enough data.

## Prerequisites

[Social media marketing fundamentals](social-media-marketing-fundamentals.md). [Product selection](../e-commerce/product-selection.md#unit-economics) for break-even ROAS.

## Core concepts

### Definition

*Paid social advertising* is the purchase of advertising on social media platforms, targeted by audience characteristics, interests, behavior or similarity to existing customers, and optimized by the platform toward a chosen objective. Ads appear in feeds, stories, short video, search results within the platform or partner apps.

*Analogy.* Paid social is like hiring a very fast, very well-informed salesperson who works in a huge market hall and is paid by how many people you want them to approach. You tell them what result you want (sales, sign-ups), give them the samples (the ad) and a budget. They learn quickly which visitors respond and focus on people like them. The analogy breaks because the salesperson keeps their methods and most of what they learn secret, reports their own success, and is employed by the market hall, whose interest is that you keep spending.

### Campaign structure

Most platforms use three levels:

| Level | What you set | Example |
| --- | --- | --- |
| Campaign | Objective | Sales (conversions), leads, traffic, awareness, engagement |
| Ad set (ad group) | Audience, budget, schedule, placements, optimization event | Women 25 to 45 in Poland interested in running, optimize for purchases |
| Ad | Creative and copy | Video, image or carousel with text, headline and call to action |

### Objectives and optimization

The objective tells the platform what to optimize for. If you choose "traffic", the system finds people who click. If you choose "purchases", it finds people likely to buy, which usually costs more per click and less per sale. Optimization needs data: Meta describes a *learning phase* after launch or significant edits, and practitioners commonly cite about 50 optimization events per ad set within seven days as the level at which delivery stabilizes. Significant changes to budget, audience or creative can restart learning.

### Audiences

- **Broad targeting:** let the algorithm find buyers within a country and age range, increasingly recommended by platforms.
- **Interest and behavior targeting:** people the platform associates with topics.
- **Custom audiences:** people who visited your site, engaged with your content or are on your customer list (requires a lawful basis and, in the EU, appropriate consent and transparency).
- **Lookalike audiences:** people similar to your customers.
- **Exclusions:** existing customers for acquisition campaigns.

### Creative

The creative (image, video, copy) is often the most important lever, because the algorithm finds audiences on its own but cannot improve a weak ad. Ads that look and feel native to the platform (for example simple vertical video that shows the product in use) often perform better than polished commercials. Testing several creatives with different hooks and angles is standard practice (see [social content creation](social-content-creation.md#the-hook) and [copywriting frameworks](../copywriting/copywriting-frameworks.md)).

### Measurement and tracking

- **Pixel:** a script on the website that reports events (view, add to cart, purchase) to the platform.
- **Conversions API (server-side):** sends events from the shop's server to the platform. It became important after browser and device privacy changes.
- **App Tracking Transparency (ATT):** since iOS 14.5 (April 2021), apps on Apple devices must ask users for permission to track them across other companies' apps and websites. Many users decline. Meta responded with Aggregated Event Measurement and statistical modeling, and default attribution windows became shorter (7-day click, 1-day view). Reported conversions became less complete and more modeled.
- **Platform-reported results** use the platform's own attribution and can overlap with other channels. Compare with total revenue and run incrementality tests where possible (see [measuring content performance](../content-marketing/measuring-content-performance.md#incrementality)).

In the EU, placing pixels and similar trackers generally requires prior consent under the ePrivacy rules, and sending customer data to platforms requires a GDPR legal basis.

### Testing products with ads

The source notes describe a test for private label products: run ads for at least seven days at 50 dollars per day (350 dollars) to get "solid proof" of demand, and compare return on ad spend (ROAS) with what is needed to be profitable. To make such a test meaningful:

1. **Calculate break-even ROAS first** (see [product selection](../e-commerce/product-selection.md#unit-economics)).
2. **Use a conversion objective** if possible, with tracking verified.
3. **Test several creatives**, because one weak ad can make a good product look unsellable.
4. **Judge cost per purchase and ROAS** against break-even, not clicks or likes.
5. **Be aware of small numbers.** At 350 dollars, a product selling at 40 dollars with a cost per purchase near 20 dollars produces around 17 purchases, which gives a rough signal, not certainty.

### Advertising rules

- **Platform ad policies:** prohibited and restricted products (for example health claims, weapons, financial products), rules on personal attributes in ad text, special categories such as housing, employment and credit in some countries.
- **Consumer law:** ads must not mislead (see [copywriting fundamentals](../copywriting/copywriting-fundamentals.md#legal-limits)).
- **EU Digital Services Act:** platforms must show who paid for an ad and the main targeting parameters, and must not target ads to minors based on profiling or to anyone based on special categories of personal data (such as health or religion).
- **Political ads** are subject to additional EU rules (Regulation (EU) 2024/900).

## Worked example

A shop tests a new insulated lunch box (invented numbers). Price 40 euros without VAT, product and shipping cost 15 euros, payment fees 1.50 euros. Contribution before ads: 23.50 euros. Break-even ROAS: 40 / 23.50 ≈ 1.70.

**Setup:** one campaign with a purchase objective, one broad ad set (adults 25 to 55 in Germany), four creatives: (A) product demo video, (B) before and after lunch photos, (C) customer review video, (D) carousel of features. Budget 50 euros a day for 7 days.

**Results after 7 days:**

| Creative | Spend | Purchases | Revenue | ROAS |
| --- | --- | --- | --- | --- |
| A | 140 | 7 | 280 | 2.00 |
| B | 70 | 1 | 40 | 0.57 |
| C | 105 | 5 | 200 | 1.90 |
| D | 35 | 0 | 0 | 0.00 |
| Total | 350 | 13 | 520 | 1.49 |

**Interpretation:** the total is below break-even, but A and C are above it. With 7 and 5 purchases, the difference between creatives is uncertain. A reasonable next step is a second week with A and C only, a new creative variation of A, and checking the shop's total sales against the platform's reported purchases.

## Trade offs and when to use it

- **Speed and scale** versus ongoing cost: results stop when spending stops.
- **Algorithmic targeting** is effective and opaque. You trade control for performance.
- **Small budgets** give noisy results. Decide in advance what result would make you stop or continue.
- **Creative fatigue:** ads lose effect as audiences see them repeatedly. Plan new creative regularly.
- **Platform dependence:** account restrictions or policy changes can stop campaigns overnight.

## Common mistakes

- **No break-even calculation.** Fix: calculate before launching.
- **Optimizing for clicks when you want sales.** Fix: choose the objective that matches the goal.
- **Judging after a day or a handful of conversions.** Fix: wait for enough data.
- **Testing one creative.** Fix: test several angles.
- **Trusting platform numbers alone.** Fix: reconcile with your own sales data.

## Practice

1. Describe the three levels of a campaign and what is set at each.
2. Why did App Tracking Transparency change how advertisers measure results?
3. Calculate the break-even ROAS for a product priced at 60 with a contribution before ads of 24.
4. Design a seven day product test with a budget of 350, four creatives and a decision rule.

Hints: question 3: 60 / 24 = 2.5.

## Further reading

- Meta Business Help Center. About the learning phase. [facebook.com/business/help](https://www.facebook.com/business/help/112167992830700). The learning phase in Meta ads.
- Meta Business Help Center. About Conversions API. [facebook.com/business/help](https://www.facebook.com/business/help/2041148702652965). Server-side event tracking.
- Apple. User privacy and data use: App Tracking Transparency. [developer.apple.com](https://developer.apple.com/app-store/user-privacy-and-data-use/). The ATT framework.
- Regulation (EU) 2022/2065 (Digital Services Act), Articles 26 and 28. [EUR-Lex](https://eur-lex.europa.eu/eli/reg/2022/2065/oj). Ad transparency and protection of minors.

TODO: Verify the Meta help article URLs and the current learning phase guidance (the 50 events figure comes from practitioner summaries of Meta's guidance).
