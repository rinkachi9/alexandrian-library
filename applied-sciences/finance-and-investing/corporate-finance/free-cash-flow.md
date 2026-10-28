# Free cash flow (FCF)

## Summary

Free cash flow (FCF) is the cash a business generates from operations after paying for the investment needed to maintain and grow its assets. It is the money available to pay dividends, repay debt, buy other companies or fund new products. Unlike profit, it counts only actual cash movements, so it reveals cash trapped in unpaid invoices and inventory and the true cost of capital expenditure. It is the input to discounted cash flow valuation.

*This note is educational. It is not investment, tax or accounting advice.*

## Prerequisites

- [Capital expenditure (CapEx)](capital-expenditure.md)
- [EBITDA](ebitda.md)

## Core concepts

### Definition

The simplest definition is:

```text
FCF = cash flow from operations - capital expenditure
```

Starting from EBITDA, an approximate bridge is:

```text
FCF ≈ EBITDA - cash taxes - increase in net working capital - CapEx
```

Working capital matters: if receivables or inventory grow, cash is absorbed even when profit is high. In valuation, *free cash flow to the firm* (FCFF, before interest, available to all investors) is discounted at WACC, and *free cash flow to equity* (FCFE, after interest and debt flows) at the cost of equity.

### Analogy

FCF is what is left in your account at the end of the month after paying all bills and the installment on the car you bought: the money you are actually free to save, spend or use to repay debt. A large salary does not help if the car and the bills take everything.

### Mechanism

**Profit and FCF.**

| Profit (net income) | Free cash flow |
| --- | --- |
| Includes non-cash items such as depreciation | Counts only cash moving |
| Includes revenue not yet collected | Counts only cash received |
| Ignores the purchase of large assets (spread as depreciation) | Subtracts CapEx when paid |
| Tells you how much you earned | Tells you how much you can spend |

**Three strategic uses.**

1. **Self-funded growth.** Positive, growing FCF means the company can grow without banks or investors. Markets treat high-FCF businesses as high quality.
2. **Valuation.** DCF models discount future FCF, not profit (see [Discounted cash flow (DCF)](discounted-cash-flow.md)).
3. **Finding cash traps.** If EBITDA grows while FCF shrinks, cash is trapped in inventory or unpaid receivables.

The bridge from EBITDA to free cash flow:

```mermaid
flowchart LR
  E[EBITDA 1,100] --> T[- Cash taxes 120]
  T --> W[- Increase in working capital 180]
  W --> C[- CapEx 400]
  C --> F[Free cash flow 400]
```

## Worked example

Two companies with the same EBITDA of 1,100 (thousands):

```python
# Python 3.12. FCF bridge for two companies with equal EBITDA.
def fcf(ebitda, taxes, delta_wc, capex):
    return ebitda - taxes - delta_wc - capex

print("A:", fcf(1100, 120, 180, 400))
print("B:", fcf(1100, 120, 650, 900))
```

Output:

```text
A: 400
B: -570
```

Company B looks equally profitable but burns 570 of cash because its receivables and inventory grew sharply and it is building a new plant. If B cannot raise money, profit will not save it.

## Trade offs and when to use it

FCF is hard to manipulate with accounting choices and shows financial freedom directly. It is volatile from period to period and can be temporarily boosted by cutting necessary investment, so read it over several periods.

## Common mistakes

- **Judging one month or quarter.** Seasonal purchases swing FCF. Use trailing twelve months (TTM).
- **The growth illusion.** Fast-growing companies often have negative FCF from spending on customer acquisition and capacity. Acceptable with enough runway, but it is a risk to manage.
- **Starving the business.** Cutting maintenance CapEx boosts FCF now and leads to breakdowns later.

## Practice

1. Cash flow from operations 900, CapEx 350. What is FCF?
2. EBITDA is growing and FCF shrinking. Name two likely causes.
3. Why is a company with 10 million revenue and 2 million FCF often safer than one with 50 million revenue and zero FCF?

### Answers

1. 550.
2. Growing receivables or inventory (working capital) and rising CapEx.
3. Because the first generates cash it can use freely, while the second depends on outside funding.

## Further reading

- IFRS Foundation. *IAS 7 Statement of Cash Flows*. [Link](https://www.ifrs.org/issued-standards/list-of-standards/ias-7-statement-of-cash-flows/). Cash flow statement.
- Koller, T., Goedhart, M., Wessels, D. (2020). *Valuation: Measuring and Managing the Value of Companies (7th ed.)*. Wiley. Free cash flow in valuation.
- Damodaran, A. (2012). *Investment Valuation (3rd ed.)*. Wiley. FCFF and FCFE.
