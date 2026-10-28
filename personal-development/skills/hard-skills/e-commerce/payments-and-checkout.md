# Payments and checkout

## Summary

The checkout is where interest becomes revenue, and where most online shoppers give up: research collected by the Baymard Institute puts the average documented cart abandonment rate at about 70%, with unexpected extra costs as the most common reason. A good checkout shows the full price early, asks only for necessary information, allows guest purchase, offers the payment methods customers in that market actually use and feels secure. Behind it, a payment gateway and processor move the money under rules that include strong customer authentication in the EU and the PCI DSS card security standard everywhere. Chargebacks, fraud and fees are part of the cost of selling online.

## Prerequisites

[E-commerce platforms](e-commerce-platforms.md).

## Core concepts

### Definitions

- The *checkout* is the sequence of pages or steps from the cart to the order confirmation: contact details, delivery, payment, review.
- A *payment gateway* is the service that securely captures payment details on the website and passes them on for authorization.
- A *payment processor* (or acquirer) handles the transaction with the card networks and banks and settles the money to the merchant.
- A *payment service provider* (PSP) bundles these functions, often with other methods (wallets, bank transfers). Examples: Stripe, Adyen, PayPal, PayU, Przelewy24, Mollie.
- *Cart abandonment* is when a shopper adds items to the cart and leaves without buying.

*Analogy.* A checkout is the till of a shop. If the queue is long, the cashier asks for your life story, the price at the till is higher than on the shelf, or the shop does not accept your card, you put the basket down and leave. The analogy breaks because in a shop a person can help you at the till, while online every unclear field or unexpected cost is met alone, and leaving costs one click.

### Why shoppers abandon

The Baymard Institute aggregates studies of cart abandonment. Its average across about 50 studies is around 70% (70.19% in one widely cited version). In its 2023 survey of US online shoppers, the most common reasons for abandoning during checkout (excluding people who were "just browsing") included:

| Reason | Share of respondents |
| --- | --- |
| Extra costs too high (shipping, tax, fees) | about 47% |
| The site wanted me to create an account | about 25% |
| Delivery was too slow | about 24% |
| I did not trust the site with my card information | about 19% |
| Too long or complicated checkout | about 18% |
| I could not see or calculate the total cost up front | about 17% |

Figures from secondary summaries of Baymard's research, checked 2026-10. They are survey answers, so they show stated reasons, not measured causes.

### Checkout design principles

- **Show total cost early.** Shipping costs and fees visible on the product page or in the cart, not first at the last step. In the EU, the total price including taxes and the delivery costs must be shown before the order is placed (Consumer Rights Directive 2011/83/EU).
- **Guest checkout.** Offer account creation after the order, not as a condition.
- **Ask only for what is needed.** Every field costs completions. Use address autocomplete.
- **Clear progress.** Show steps and allow going back without losing data.
- **Mobile first.** Large inputs, the right keyboard for each field (numeric for card numbers), wallet payments.
- **Trust signals.** Recognizable payment logos, HTTPS, clear return policy link, contact details (see [calls to action and risk reversal](../copywriting/calls-to-action-and-risk-reversal.md)).
- **Clear order button.** In the EU, the button that places the order must be labeled with "order with obligation to pay" or an equally unambiguous phrase (Directive 2011/83/EU, Article 8(2)).
- **Error messages** that explain how to fix the problem (see [writing for the web](../copywriting/writing-for-the-web.md#microcopy)).

### Payment methods

Preferences differ strongly by country:

| Method | Examples | Notes |
| --- | --- | --- |
| Cards | Visa, Mastercard, American Express | Universal, chargeback risk, authentication rules |
| Digital wallets | Apple Pay, Google Pay, PayPal | Fast on mobile, often fewer fields |
| Local bank and instant payment methods | BLIK (Poland), iDEAL (Netherlands), Bancontact (Belgium), Przelewy24 | Dominant in some markets |
| Buy now, pay later (BNPL) | Klarna, PayPo, Afterpay | Can raise conversion and order value. Regulated as consumer credit in the EU under the new Consumer Credit Directive (EU) 2023/2225 |
| Cash on delivery | Common in some markets | Higher return and refusal risk, handling costs |
| Bank transfer and invoice | B2B orders | Payment delay and credit risk |

Offering the methods customers in your market expect is one of the simplest conversion improvements.

### Strong customer authentication

In the European Economic Area, the revised Payment Services Directive (PSD2, Directive (EU) 2015/2366) requires *strong customer authentication* (SCA) for most electronic payments initiated by the payer: two of three factors from knowledge (a PIN), possession (a phone) and inherence (a fingerprint). For card payments online this is usually done through *3-D Secure 2*, often in the bank's app. Exemptions exist, for example for low-value transactions and for transactions the provider judges low-risk. Authentication adds a step, so a smooth implementation matters.

### Card data security: PCI DSS

The *Payment Card Industry Data Security Standard* (PCI DSS), maintained by the PCI Security Standards Council, applies to every business that stores, processes or transmits card data. Most small shops reduce their scope by using hosted payment pages or embedded fields from their PSP, so card numbers never touch their own servers. Version 4.0 (and 4.0.1) added requirements that became mandatory on 31 March 2025, including requirements 6.4.3 and 11.6.1 for managing and monitoring scripts on payment pages, aimed at *e-skimming* (malicious scripts that steal card data in the browser). Merchants using fully outsourced payment pages may qualify for the simplest self-assessment questionnaire (SAQ A), subject to eligibility criteria.

### Fees, fraud and chargebacks

- **Fees.** PSPs charge per transaction, usually a percentage plus a fixed amount, varying by method, card type and region. Include them in [unit economics](product-selection.md#unit-economics).
- **Fraud.** Stolen card data is used to buy goods. PSPs offer fraud screening. Signs include mismatched billing and shipping countries, many attempts with different cards and unusually large first orders.
- **Chargebacks.** A *chargeback* is a reversal of a card payment initiated by the cardholder's bank, for example for fraud, non-delivery or "not as described". The merchant loses the payment, pays a fee and can dispute it with evidence (tracking, delivery confirmation, communication). High chargeback rates can lead to penalties or loss of the ability to accept cards.

## Worked example

A shop selling sports nutrition in Poland reviews its checkout (invented data).

**Analytics:** 3,200 carts started per month, 1,050 orders, so 67% abandonment. Of those who reach the payment step, 30% leave.

**Audit findings:**

1. Shipping cost (14.99 PLN) appears only at the last step.
2. Account creation is required.
3. Payment options: cards and bank transfer only. No BLIK.
4. The phone field rejects numbers with spaces without explanation.

**Changes:**

1. Shipping cost and free shipping threshold shown in the cart and on product pages.
2. Guest checkout, with an optional account after the order.
3. BLIK added through the existing PSP.
4. Phone field accepts spaces, error message explains the format.

**Measurement:** an A/B test is not feasible for all changes at once with this traffic, so the shop compares the next eight weeks with the previous eight and with the same period last year. Payment step abandonment falls to 21%. The comparison cannot separate the effect of each change, and seasonality may contribute.

## Trade offs and when to use it

- **More payment methods** raise conversion but add fees, integration work and reconciliation effort. Add the ones your customers use.
- **Fraud screening** reduces fraud and also blocks some genuine customers. Tune it with data.
- **BNPL** can increase order value and attracts customers who may overspend. Consider your audience and the reputational and regulatory context.
- **One-page versus multi-step checkout.** Neither is always better. Clarity and the number of fields matter more than the number of pages.

## Common mistakes

- **Surprise costs at the last step.** Fix: show all costs early.
- **Forced account creation.** Fix: guest checkout.
- **Missing local payment methods.** Fix: check market preferences.
- **Handling card data yourself without need.** Fix: use hosted payment fields to reduce PCI scope.
- **Ignoring chargebacks.** Fix: keep delivery evidence and respond to disputes.

## Practice

1. What does a payment gateway do, and how does it differ from a processor?
2. Name the three most common reasons for checkout abandonment in Baymard's 2023 survey.
3. What is strong customer authentication, and which law requires it in the EU?
4. What do PCI DSS requirements 6.4.3 and 11.6.1 address?
5. Audit the checkout of a shop you use and list five improvements.

## Further reading

- Baymard Institute. Cart abandonment rate statistics. [baymard.com](https://baymard.com/lists/cart-abandonment-rate). Aggregated abandonment rates and reasons.
- Directive (EU) 2015/2366 (PSD2). [EUR-Lex](https://eur-lex.europa.eu/eli/dir/2015/2366/oj). Strong customer authentication.
- PCI Security Standards Council. PCI DSS v4.0.1 and guidance on requirements 6.4.3 and 11.6.1. [pcisecuritystandards.org](https://www.pcisecuritystandards.org/). The card data security standard.
- Directive 2011/83/EU on consumer rights, Article 8. [EUR-Lex](https://eur-lex.europa.eu/eli/dir/2011/83/oj). Price information and the order button.
- Directive (EU) 2023/2225 on credit agreements for consumers. [EUR-Lex](https://eur-lex.europa.eu/eli/dir/2023/2225/oj). New EU consumer credit rules that cover many BNPL products.

TODO: Confirm the Baymard figures on baymard.com directly (they come from secondary summaries) and the application date of Directive (EU) 2023/2225.
