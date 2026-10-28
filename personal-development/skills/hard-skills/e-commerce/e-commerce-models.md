# E-commerce models

## Summary

E-commerce (electronic commerce) is buying and selling goods or services over the internet, including the transfer of money and data that completes the transaction. Transactions are classified by who sells to whom: business to business (B2B), business to consumer (B2C), consumer to consumer (C2C), consumer to business (C2B) and transactions with public administration. In the United States, e-commerce was about 17% of all retail sales in the second quarter of 2026. Running an online store involves far more than a website: platforms, payments, fulfillment, customer service, data protection, analytics and, for cross-border sales, customs and tax.

## Prerequisites

None. This note is the entry point to [e-commerce](README.md).

## Core concepts

### Definition

*E-commerce* is any commercial transaction in which the order is placed over the internet, whether the product is physical (a book), digital (software) or a service (a booked haircut). Payment and delivery may happen online or offline. *Mobile commerce* (m-commerce) is the part of e-commerce carried out on phones and tablets.

*Analogy.* An online shop is a shop whose counter is a web page. Behind the counter there is still a warehouse, a till, a delivery van and someone who answers complaints. The analogy holds for the work behind the counter, which does not disappear online. It breaks because an online counter can serve customers in many countries at once, which brings in foreign tax and consumer law that a local shop never meets.

### Business model and transaction model

A *business model* describes how a company creates value for customers and captures part of it as revenue: what it sells, to whom, through which channels, and how it makes money. Examples from the source notes: Apple sells devices directly to consumers, Uber connects drivers with riders and takes a fee, Google and Meta (Facebook) sell advertising. The theory of business models belongs to business and management (Osterwalder and Pigneur, 2010; Teece, 2010).

A *transaction model* is narrower. It classifies e-commerce by the parties on each side of a sale.

### Transaction models

| Model | Seller to buyer | Example from the source notes | Typical features |
| --- | --- | --- | --- |
| B2B | Business to business | A car manufacturer buying tyres from a tyre maker | Large orders, negotiated prices, invoices, repeat relationships |
| B2C | Business to consumer | An online retailer such as Amazon selling to the public | Many small orders, listed prices, consumer protection law applies |
| C2C | Consumer to consumer | Selling old furniture on Craigslist or eBay | A platform connects private sellers and buyers and takes a fee |
| C2B | Consumer to business | Freelancers offering services to companies on Upwork | Individuals sell work, content or data to businesses |
| B2A (B2G) | Business to administration (government) | A company paying taxes or applying for permits online, or bidding in public procurement | Formal procedures, public tenders |
| C2A (C2G) | Consumer to administration (government) | Paying taxes, fines or tuition online | Mostly payments and applications |

Marketplaces such as Amazon and eBay host several models at once: Amazon sells its own stock (B2C) and lets third-party businesses sell (B2C through a marketplace), and eBay hosts both business and private sellers. A newer label, *D2C* (direct to consumer), describes brands that sell their own products to consumers without retailers in between.

### The parts of an e-commerce business

The source notes list the areas a seller has to understand. Each is a field of its own:

1. **Platforms.** Hosted store builders (Shopify), plugins for a website (WooCommerce on WordPress), and marketplaces (Amazon, eBay, Allegro, Etsy). The choice trades control against reach and fees (see [e-commerce platforms](e-commerce-platforms.md)).
2. **Traffic and marketing.** Search engine optimization (see [e-commerce SEO](../search-engine-optimization/e-commerce-seo.md)), paid ads (see [paid social advertising](../social-media/paid-social-advertising.md)), [email marketing](../content-marketing/email-marketing.md) and [content marketing](../content-marketing/content-marketing-fundamentals.md).
3. **Mobile commerce.** Most consumer browsing is on phones, so the store must work well on small screens.
4. **Payment gateways.** Services that accept cards, wallets (PayPal, Apple Pay, Google Pay), bank transfers and local methods (BLIK in Poland, iDEAL in the Netherlands). Card data security is governed by the industry standard PCI DSS, and in the EU most online card payments need strong customer authentication under the second Payment Services Directive (PSD2) (see [payments and checkout](payments-and-checkout.md)).
5. **Shipping and fulfillment.** Storing, packing and delivering, done by the seller, a fulfillment provider or the supplier (see [fulfillment and shipping](fulfillment-and-shipping.md) and [dropshipping](dropshipping.md)).
6. **Customer service.** Answering questions, handling complaints, returns and refunds (see [customer service and returns](customer-service-and-returns.md)).
7. **Data privacy and security.** In the EU the General Data Protection Regulation (GDPR, Regulation 2016/679) governs personal data, and the ePrivacy rules govern cookies (see [e-commerce law and cross-border](e-commerce-law-and-cross-border.md)).
8. **Analytics.** Measuring traffic, conversion rate, average order value and customer lifetime value to improve sales (see [e-commerce metrics](e-commerce-metrics.md)).
9. **International e-commerce.** Currency, language, delivery, returns, VAT and customs (see [e-commerce law and cross-border](e-commerce-law-and-cross-border.md)).

### Size of the market

The US Census Bureau estimated US retail e-commerce sales at 340.2 billion dollars in the second quarter of 2026, seasonally adjusted, which was 17.1% of total retail sales, up from 16.3% a year earlier (release of 18 August 2026). Retail e-commerce in these statistics excludes services such as travel and B2B sales, which are much larger in value. Figures checked 2026-10 through search summaries of the release.

## Worked example

Classifying four transactions:

1. A bakery orders 50 kg of flour every week from a wholesaler's online portal. **B2B**: both parties are businesses, prices are negotiated, the wholesaler invoices monthly.
2. A student buys headphones from an electronics retailer's website. **B2C**: consumer law applies, including in the EU a 14 day right of withdrawal.
3. The same student later sells the headphones on a second-hand platform. **C2C**: the platform handles payment and takes a commission. EU consumer law generally does not protect the buyer against a private seller in the same way.
4. A freelance designer sells logo design to a startup through a freelance platform. **C2B**: an individual sells a service to a business.

The classification matters because it decides which rules apply (consumer protection, VAT, invoicing) and what the buyer expects (price lists or negotiation, card payment or invoice).

## Trade offs and when to use it

- **B2C** reaches many buyers but faces strong competition, high marketing costs and strict consumer law.
- **B2B** has fewer, larger and more loyal customers, but longer sales cycles and price negotiation.
- **Marketplaces** give immediate traffic and trust in exchange for fees, rules and little control over the customer relationship.
- **Own store** gives control and customer data but requires building traffic from zero.

## Common mistakes

- **Thinking e-commerce is "just a website".** Fix: plan fulfillment, payments, service and legal obligations before launch.
- **Treating C2C rules as if they applied to a business.** A person who sells regularly for profit is usually a trader under consumer law, with the obligations that follow. Fix: check when your activity becomes a business in your country.
- **Ignoring cross-border rules.** Fix: check VAT, customs and consumer law for every target country.

## Practice

1. What is the difference between a business model and a transaction model?
2. Classify: a municipality buying laptops through an online tender; a person selling photos to a stock photo agency; a company selling software subscriptions to individuals.
3. Name the nine areas of an e-commerce business from this note and say which one you know least about.

Hints: question 2 involves B2A (B2G), C2B and B2C.

## Further reading

- U.S. Census Bureau. Quarterly Retail E-Commerce Sales, 2nd Quarter 2026. [census.gov](https://www.census.gov/retail/ecommerce.html). The official US estimate of e-commerce share of retail.
- Osterwalder, A., & Pigneur, Y. (2010). *Business Model Generation*. Wiley. The business model canvas, a widely used way to describe business models.
- Teece, D. J. (2010). Business models, business strategy and innovation. *Long Range Planning*, 43(2-3), 172-194. [doi:10.1016/j.lrp.2009.07.003](https://doi.org/10.1016/j.lrp.2009.07.003). A research view of what a business model is.
- Regulation (EU) 2016/679 (General Data Protection Regulation). [EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj). The EU rules on personal data.

TODO: The census.gov release could not be opened from the working environment. Confirm the Q2 2026 figures (340.2 billion dollars, 17.1%) on the release itself.
