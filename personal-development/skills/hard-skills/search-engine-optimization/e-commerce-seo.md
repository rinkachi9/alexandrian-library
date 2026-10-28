# E-commerce SEO

## Summary

E-commerce SEO applies search engine optimization to online shops, whose most valuable pages are category pages and product pages. Shops face problems that ordinary sites do not: thousands of similar products, the same item reachable under many URLs, filters that create endless combinations of pages, products that sell out, and descriptions copied from the manufacturer. The work is to target commercial queries with category pages, make each product page unique and informative, control duplicates and filter URLs, and give search engines structured product data such as price and availability.

## Prerequisites

[how search engines work](how-search-engines-work.md) for crawling, indexing, keywords and links. [E-commerce models](../e-commerce/e-commerce-models.md) for the business context.

## Core concepts

### Definition

*E-commerce SEO* is the process of increasing the visibility of an online store in search engine results, so that people searching for products, product types or product problems find the store without paid ads. The source notes describe it as fine-tuning the site to search engine best practices and updating content to reflect what customers search for. Its benefits are more visitors, brand awareness and sales, at the cost of continuous work as products and search engines change.

*Analogy.* A shop's SEO is like the layout and signage of a large department store. Category pages are the floor directory and the department signs. Product pages are the labels on the shelves. Filters are the store staff who can show "only blue shirts in size M", useful for a customer but not something you print on the floor directory for every combination. The analogy breaks because in a real store a customer can always walk the aisles, while a search engine sees only the pages you let it crawl and index.

### Keyword mix

Most content sites target *informational* queries ("how to fold a t-shirt"). A shop needs a mix:

- **Commercial and transactional queries** for category and product pages: "linen shirts men", "glass jar blender 450w".
- **Informational queries** for guides and blog posts that lead to products: the source's example is a t-shirt shop writing about how to fold t-shirts without wrinkles.

Autocomplete in Amazon is particularly useful for shops because its suggestions are product oriented and include attributes buyers filter by.

### Category pages

*Category pages* (also called collection pages) usually target the broadest and most valuable commercial queries. Make them strong by:

- a clear title tag and heading with the category name buyers use,
- a short, useful introduction (what to look for, sizes, materials), placed so it does not push products below the screen,
- links to subcategories and to buying guides,
- a stable URL that does not change when products change.

### Product pages

Search engines use a page's content to decide what it is about and how high it should rank. A product page with one line of text and a photo gives them little to work with. Copying the description from the manufacturer or supplier creates *duplicate content*: many shops have the same text, and the search engine has no reason to prefer yours.

A strong product page has:

- an original description written for the buyer, with benefits and specifications (see [copywriting](../copywriting/value-proposition-and-benefits.md#features-benefits-and-outcomes)),
- several good photos with descriptive alt text and file names,
- a specification table,
- genuine customer reviews and questions,
- shipping, return and warranty information,
- structured data (below).

### Duplicate URLs and faceted navigation

*Faceted navigation* is the set of filters on a category page: color, size, price, brand, sort order. Each combination can produce a separate URL, so a category with ten filters can generate a very large number of near-identical pages. Google's documentation on faceted navigation (made official guidance in December 2024) notes that such duplicate URLs waste crawling and server resources. Common approaches:

- Let a few valuable filter pages that match real searches ("black running shoes") be indexable, with their own title and introduction.
- Point the canonical URL of other filter combinations to the main category page.
- Prevent crawling of filter combinations that never have search value, for example with robots.txt rules on their parameters, and avoid linking to them with crawlable links.
- Keep sort order and tracking parameters out of the index.

The same product listed under several category paths should have one canonical URL. Platforms such as Shopify add canonical tags automatically, but check the result.

### Product variants and out-of-stock items

- **Variants** (sizes, colors) are usually one product page with options, unless a variant is searched for on its own.
- **Temporarily out of stock:** keep the page, show the status, offer a notification and keep availability in the structured data up to date.
- **Permanently discontinued:** redirect (HTTP 301) to the closest replacement or the category, or return a 404 or 410 status if nothing fits. Avoid redirecting everything to the home page.

### Structured data

*Structured data* is machine readable information added to a page, usually with the schema.org vocabulary in JSON-LD format. For shops, the `Product` type with `Offer` (price, currency, availability) and, where they exist, `AggregateRating` and `Review` lets Google show price, availability and ratings in results and in shopping surfaces. A product feed in Google Merchant Center is another way to supply the same data. Structured data must match what the page shows. Marking up reviews that are not on the page violates Google's guidelines.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Glass jar blender 450 W",
  "image": "https://example.com/images/blender-450w.jpg",
  "sku": "BL-450-G",
  "offers": {
    "@type": "Offer",
    "price": "89.00",
    "priceCurrency": "EUR",
    "availability": "https://schema.org/InStock"
  }
}
</script>
```

The example is untested against Google's Rich Results Test. Run it through the test before using it.

### Platform features

The source notes list what Shopify handles automatically: canonical tags, `sitemap.xml` and `robots.txt` files, title tags that include the store name, and social sharing options. What remains manual: titles, meta descriptions, image alt text, file names and the URLs of products, collections and blog posts. Other platforms (WooCommerce, Magento, marketplaces) differ, so check what yours generates. Checked against the source notes only, not against current Shopify documentation.

### Content and links for shops

- **Buying guides and how-to articles** target informational queries and link to categories.
- **Original data** (a survey of customers, a test of products) attracts links from press and blogs.
- **Press mentions** can be earned by answering journalists' requests for expert sources and by offering a genuine story. Paid placements must be marked as sponsored.

## Worked example

A shop sells 400 kinds of loose leaf tea. Search Console shows 40,000 indexed URLs, most of them filter pages such as `/green-tea?origin=japan&sort=price&caffeine=low`.

1. **Diagnosis.** Only about 450 URLs (categories and products) are meant to rank. The rest are filter combinations that compete with each other and use up crawling.
2. **Valuable filters.** Keyword research shows real demand for "Japanese green tea" and "decaf green tea". The shop creates two indexable pages for these with their own titles and introductions.
3. **Other filters.** Canonical URLs point to the main category. Sort and tracking parameters are excluded from crawling. Filter links for low value combinations are changed so they are not crawlable links.
4. **Product pages.** The 50 best-selling teas get original descriptions with brewing temperature, taste notes and origin, replacing supplier text.
5. **Structured data.** `Product` and `Offer` data are added and tested.
6. **Result to watch.** Over three months: number of indexed URLs, impressions and clicks for category queries, and crawling statistics.

All numbers are invented to show the process.

## Trade offs and when to use it

- **Original descriptions cost time.** Prioritize products by revenue and search demand.
- **Indexable filter pages** can win long-tail queries but multiply maintenance. Choose few, based on real demand.
- **Marketplaces versus own store.** Selling on Amazon or eBay uses their search and traffic, at the price of fees and less control. Your own store needs SEO but builds an asset.
- **Search is only one channel.** Many shops rely more on paid social, email or marketplaces. SEO is a long-term investment.

## Common mistakes

- **Supplier descriptions on every product.** Fix: rewrite the most important products first.
- **Letting every filter combination be indexed.** Fix: index only filter pages with real search demand.
- **Deleting sold-out products without a redirect.** Fix: keep temporarily unavailable pages, redirect permanent removals to the closest match.
- **Structured data that does not match the page.** Fix: generate it from the same data the page shows.
- **Thin category pages.** Fix: add a short, useful introduction and clear subcategory links.

## Practice

1. Why is a supplier's product description a problem for SEO?
2. A category has filters for color, size and price. Which filter pages would you make indexable, and how would you decide?
3. What should happen to the URL of a product that is discontinued forever?
4. Write `Product` structured data for a product you know and test it in Google's Rich Results Test.

## Further reading

- Google Search Central. Managing crawling of faceted navigation URLs. [developers.google.com](https://developers.google.com/search/docs/crawling-indexing/crawling-managing-faceted-navigation). Google's guidance on filters.
- Google Search Central. Product structured data. [developers.google.com](https://developers.google.com/search/docs/appearance/structured-data/product). Required and recommended properties.
- Google Search Central. Consolidate duplicate URLs. [developers.google.com](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls). How canonicalization works.
- schema.org. Product. [schema.org](https://schema.org/Product). The vocabulary used for product data.

TODO: The Google Search Central pages were not reachable from the working environment. Read them and confirm the faceted navigation recommendations, the December 2024 date and the current Product structured data requirements.
TODO: Verify the list of automatic SEO features against current Shopify documentation.
