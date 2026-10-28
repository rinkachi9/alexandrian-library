# E-commerce platforms

## Summary

An e-commerce platform is the software that runs an online store: product catalog, cart, checkout, payments, orders and customer accounts. The main choice is between selling on a marketplace (Amazon, eBay, Allegro, Etsy), which brings ready traffic and trust in exchange for fees, rules and little control over customers, and running your own store, either on a hosted platform (Shopify and similar) or on self-hosted open source software (WooCommerce, Magento Open Source and others). Most growing sellers combine channels. The right choice depends on the product, the budget, the technical skills available, and how much control over brand and customer data matters.

## Prerequisites

[E-commerce models](e-commerce-models.md).

## Core concepts

### Definition

An *e-commerce platform* is a software system that provides the functions needed to sell online: a storefront, product and inventory management, a cart and checkout, payment integration, order management, customer accounts, and usually tools for discounts, shipping rates, taxes and analytics. A *sales channel* is any place where the products are sold: the own store, a marketplace, a social shop, a physical point of sale.

*Analogy.* Choosing a platform is like choosing where to open a shop. A stall in a busy shopping mall (marketplace) gets visitors from day one, but the mall sets the rules, takes a share of each sale and owns the relationship with shoppers. A rented shop on a high street with a landlord who maintains the building (hosted platform) gives you your own front door and sign for a monthly rent. Building your own shop on your own land (self-hosted) gives full control and full responsibility for the roof. The analogy breaks because online you can be in all three places at once with the same stock, which physical shops cannot.

### Marketplaces

A *marketplace* is a platform where many sellers offer products to the marketplace's customers. Examples: Amazon, eBay, Allegro (Poland), Etsy (handmade and vintage), Zalando (fashion, partner program), Temu and AliExpress (cross-border).

| Benefits | Costs and risks |
| --- | --- |
| Large existing audience and search traffic | Commission on each sale, often plus fees for listings, fulfillment and advertising |
| Built-in trust, payments and buyer protection | Strict rules on listings, prices, delivery times and returns. Account suspension risk |
| Optional fulfillment services | Direct competition next to your listing, including the marketplace's own products |
| Fast start | Limited brand presentation, little access to customer data, hard to build a relationship |

Fee structures change often and differ by category and country, so check the current fee pages before calculating margins.

### Hosted platforms

A *hosted* (software as a service, SaaS) platform runs the store on the provider's infrastructure for a monthly fee, sometimes plus transaction fees. Examples: Shopify, BigCommerce, Wix, Squarespace, and regional providers such as Shoper (Poland).

- **Strengths:** fast setup, security and updates handled by the provider, app ecosystems, built-in checkout and payment options, hosting that scales.
- **Limits:** less control over checkout and code, costs that grow with apps and add-ons, dependence on the provider's rules and pricing, platform-specific limits on customization.

### Self-hosted open source platforms

*Self-hosted* platforms are software you install and run on your own hosting. Examples: WooCommerce (a WordPress plugin), PrestaShop, Magento Open Source (Adobe Commerce is the paid version).

- **Strengths:** full control over code, data and design, no platform transaction fees, large plugin ecosystems.
- **Limits:** you are responsible for hosting, security updates, backups, performance and payment security compliance. Costs move from subscriptions to developer time.

### Headless commerce

*Headless* commerce separates the front end (what customers see) from the commerce back end (catalog, cart, orders), connected through APIs. It allows custom front ends, multiple channels and high performance, at the cost of more development. It suits larger stores with development teams.

### Choosing a platform

| Criterion | Questions |
| --- | --- |
| Product and audience | Do your buyers search on a marketplace first? Is the product a commodity or a brand? |
| Catalog size and complexity | How many products and variants? Configurable products? B2B price lists? |
| Payments | Does the platform support the payment methods your customers use (cards, BLIK, iDEAL, PayPal, buy now pay later)? |
| Markets | Multi-currency, multi-language, tax handling for several countries? |
| Integrations | Accounting, inventory, shipping carriers, marketplaces, email marketing? |
| Total cost | Subscription, transaction fees, apps, themes, development, hosting, payment fees |
| Skills | Who will run and maintain it? |
| Exit | Can you export products, customers and orders if you leave? |

### Multichannel selling

Many sellers combine an own store with one or two marketplaces and social shops. This spreads risk and reaches more buyers, but requires synchronized inventory (to avoid selling stock you no longer have), consistent pricing rules and more customer service. Inventory and order management software connects the channels.

### Mobile

Most consumer browsing happens on phones, so the store must be designed mobile-first: fast pages, large tap targets, simple navigation and a short checkout. The source notes stress mobile responsiveness as a criterion of a good store.

## Worked example

A small brand of natural soaps chooses its setup (all numbers invented, fees are placeholders to be checked).

- **Situation:** 40 products, sales mainly in Poland, a founder with no developer, a budget of about 300 PLN a month for software.
- **Option A, marketplace only (Allegro).** Fast sales from day one. Commission on each sale reduces margin. Limited brand story. No customer email list.
- **Option B, hosted store (Shopify or Shoper).** Monthly fee plus apps, full brand presentation, own customer data, but no traffic at start.
- **Option C, WooCommerce.** Low software cost, but the founder would need to pay a developer for setup and maintenance and handle security.

**Decision:** start with a hosted store for the brand and email list, plus a marketplace account for a subset of best-selling products to reach buyers who search there. Product inserts in marketplace orders invite buyers to the brand's newsletter, within the marketplace's rules on contacting buyers.

**Review after six months:** compare margin per channel after fees and advertising, and the share of repeat customers.

## Trade offs and when to use it

- **Marketplace first** when buyers search there, the product is a known type and you need sales quickly.
- **Own store first** when the brand story and customer relationship matter, and you can drive traffic through content, social media or ads.
- **Hosted** when time and simplicity matter more than control.
- **Self-hosted** when you have technical resources and need flexibility or want to avoid platform fees.
- **Switching later is expensive.** Migration means moving products, customers, URLs (with redirects, see [technical SEO](../search-engine-optimization/technical-seo.md)) and integrations.

## Common mistakes

- **Choosing by subscription price alone.** Fix: calculate total cost including fees, apps and time.
- **Ignoring local payment methods.** Fix: check what your customers actually use.
- **Building only on a marketplace.** Fix: plan how to build an owned relationship within the marketplace's rules.
- **Overselling across channels.** Fix: synchronize inventory.
- **No export path.** Fix: check data export before choosing.

## Practice

1. Compare a marketplace, a hosted platform and a self-hosted platform on control, cost, traffic and responsibility.
2. List the costs that make up the total cost of a hosted store.
3. For a product you know, decide which channel mix you would start with and why.
4. What is headless commerce, and when is it worth its cost?

## Further reading

- Shopify Help Center. [help.shopify.com](https://help.shopify.com/). Documentation of a common hosted platform.
- WooCommerce documentation. [woocommerce.com](https://woocommerce.com/documentation/). Documentation of a common self-hosted platform.
- Amazon Seller Central. Selling fees. [sell.amazon.com](https://sell.amazon.com/pricing). An example of marketplace fee structures.

TODO: Add a research or market report source on platform market shares and on the share of mobile in e-commerce traffic, with a date.
