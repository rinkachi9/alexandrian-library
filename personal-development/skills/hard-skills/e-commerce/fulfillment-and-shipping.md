# Fulfillment and shipping

## Summary

Fulfillment is everything between a paid order and a delivered parcel: receiving and storing stock, picking and packing orders, shipping them and handling what comes back. A seller can do it in-house, outsource it to a third-party logistics provider (3PL), use a marketplace's fulfillment service, or let suppliers ship directly (dropshipping). Delivery speed, cost and reliability strongly affect whether people buy and whether they come back, and shipping is often one of the largest costs per order. Inventory management, forecasting how much stock to hold and when to reorder, is the other half of the skill.

## Prerequisites

[E-commerce platforms](e-commerce-platforms.md). The supplier side is in [supplier sourcing](supplier-sourcing.md).

## Core concepts

### Definition

*Fulfillment* is the process of receiving, storing, picking, packing and shipping customer orders, and processing returns. *Logistics* is the wider management of the flow of goods. *Inventory management* is deciding how much stock to hold, where, and when to reorder.

*Analogy.* Fulfillment is the kitchen of a restaurant. Customers never see it, but they taste its results: the wrong dish, a cold plate or a long wait spoil the evening however good the menu. A small restaurant can have the owner cook. A busy one needs a brigade, or a central kitchen that delivers. The analogy breaks because a restaurant cooks to order, while most online sellers must buy and store goods before anyone orders them, which brings the risk of running out or being left with unsold stock.

### Fulfillment models

| Model | Who stores and ships | Fits | Trade off |
| --- | --- | --- | --- |
| In-house | The seller | Small volume, special handling, early stage | Control and low fixed cost, but time-consuming and hard to scale |
| Third-party logistics (3PL) | A specialist warehouse | Growing volume, multiple channels | Professional and scalable, fees per order and storage, less direct control |
| Marketplace fulfillment | The marketplace (for example Fulfillment by Amazon) | Selling mainly on that marketplace | Fast delivery badges, but fees, strict inbound rules and dependence |
| Dropshipping | The supplier | Testing products, no stock | No inventory risk, little control over speed and quality (see [dropshipping](dropshipping.md)) |
| Local fulfillment from a sourcing agent or local warehouse | Agent or warehouse near customers | The third level of dropshipping in the source notes | Faster delivery, requires buying stock |

### The order-to-delivery process

1. **Receiving:** goods arrive, are counted and checked against the purchase order.
2. **Storage:** each product (*SKU*, stock keeping unit) has a location.
3. **Picking:** collecting the items for an order.
4. **Packing:** choosing packaging, protecting items, adding documents and inserts.
5. **Labeling and handover** to the carrier.
6. **Tracking:** the customer receives a tracking link.
7. **Delivery:** to the address, a parcel locker or a pick-up point.
8. **Returns processing:** checking returned items, restocking or disposing (see [customer service and returns](customer-service-and-returns.md)).

### Shipping options and costs

- **Carriers:** national postal services, courier companies and parcel locker networks (in Poland, parcel lockers are a very popular delivery method).
- **Price factors:** weight, dimensions (*dimensional weight*: large light parcels are charged as if heavier), distance, speed, insurance and volume discounts.
- **Delivery promises** must be realistic. Customers expect a delivery estimate before ordering, and legal rules apply to delivery times (see [e-commerce law and cross-border](e-commerce-law-and-cross-border.md)).

### Shipping pricing strategies

| Strategy | Effect |
| --- | --- |
| Free shipping on all orders | Removes a top reason for abandonment, cost goes into the product price |
| Free shipping over a threshold | Raises average order value. Set the threshold above the current average order |
| Flat rate | Simple and predictable |
| Real-time carrier rates | Accurate, but can show surprising amounts at checkout |
| Paid express option | Customers who need speed pay for it |

Unexpected extra costs, including shipping, are the most common stated reason for abandoning checkout in Baymard Institute surveys (see [payments and checkout](payments-and-checkout.md#why-shoppers-abandon)).

### Packaging

Packaging protects the product, affects shipping cost (size and weight), and is part of the customer experience. Over-sized boxes raise costs and annoy customers. EU rules on packaging and packaging waste (Regulation (EU) 2025/40, applying in stages from 2026) set requirements on minimizing packaging, empty space and recyclability. National rules on extended producer responsibility can require registration and fees for packaging placed on the market.

### Inventory management

Key concepts:

- **Lead time:** time from placing an order with the supplier to receiving the goods.
- **Reorder point:** the stock level at which you reorder, roughly expected sales during the lead time plus safety stock.
- **Safety stock:** extra stock to cover variation in demand and lead time.
- **Stockout:** running out, which loses sales and can hurt marketplace rankings.
- **Overstock:** excess stock that ties up cash and may need to be discounted.
- **Inventory turnover:** how many times stock is sold and replaced in a period.

A simple reorder point:

reorder point = average daily sales × lead time in days + safety stock

The source notes list effective inventory management, avoiding stockouts and backorders, as a criterion of a winning product.

## Worked example

A shop sells about 12 units a day of its best-selling product (invented numbers). The supplier's lead time is 30 days. Daily sales vary between about 8 and 18.

- Expected sales during lead time: 12 × 30 = 360 units.
- Safety stock: the shop chooses 10 days of average sales to cover variation and delays: 120 units.
- Reorder point: 360 + 120 = 480 units. When stock drops to 480, the shop places a new order.
- Order quantity: the supplier's MOQ is 500, and the shop orders 900 to cover about 75 days of sales, balancing storage cost with the shipping cost per order.

**Shipping choice.** Average order value is 95 PLN. Most orders weigh under 2 kg. The shop offers parcel lockers at 12.99 PLN and courier at 16.99 PLN, free over 150 PLN. After two months, average order value rises to 112 PLN, as more customers add items to reach the threshold. Seasonality and other changes may also contribute.

A statistical safety stock uses the variability of demand and lead time. The 10 day rule here is a simple heuristic.

## Trade offs and when to use it

- **In-house versus outsourced.** In-house keeps control and saves fees at low volume, and consumes time that could go to sales and products. Outsourcing pays off when volume makes in-house packing a bottleneck.
- **Speed versus cost.** Faster delivery raises conversion and costs more. Offer options.
- **More stock versus cash.** Higher safety stock prevents stockouts and ties up money. Products with uncertain demand need smaller orders.
- **Free shipping** helps conversion and must be paid for somewhere: price, margin or threshold.

## Common mistakes

- **Unrealistic delivery promises.** Fix: promise what you can deliver in most cases.
- **Ignoring dimensional weight.** Fix: right-size packaging.
- **No reorder point.** Fix: calculate it and set alerts.
- **Overselling across channels.** Fix: synchronize inventory.
- **Surprise shipping costs at checkout.** Fix: show them early.

## Practice

1. Compare in-house fulfillment, a 3PL and marketplace fulfillment on control, cost and scalability.
2. Calculate the reorder point for a product with average sales of 5 a day, a lead time of 20 days and 7 days of safety stock.
3. How would you choose a free shipping threshold?
4. List the steps of the order-to-delivery process.

Hints: question 2: 5 × 20 + 5 × 7 = 135 units.

## Further reading

- Baymard Institute. Cart abandonment rate statistics. [baymard.com](https://baymard.com/lists/cart-abandonment-rate). The role of shipping costs and speed in abandonment.
- Regulation (EU) 2025/40 on packaging and packaging waste. [EUR-Lex](https://eur-lex.europa.eu/eli/reg/2025/40/oj). EU packaging rules.

TODO: Verify the application dates of Regulation (EU) 2025/40 and add a logistics textbook source for reorder point and safety stock calculations.
