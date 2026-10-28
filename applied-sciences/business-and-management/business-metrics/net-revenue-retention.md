# Net revenue retention

## Summary

Net revenue retention (NRR) measures how much recurring revenue a group of existing customers generates now compared with a year (or month) ago, including expansion, contraction and churn but excluding new customers. Above 100%, existing customers grow faster than losses: the business has negative net churn and would grow even without any new customers. NRR is one of the metrics investors watch most closely in subscription businesses, because it combines retention and expansion in one number.

## Prerequisites

- [Churn rate](churn-rate.md)

## Core concepts

### Definition

*Net revenue retention* (also *net dollar retention*) is:

```text
NRR = (starting MRR + expansion - contraction - churned MRR) / starting MRR
```

measured for the customers who were active at the start of the period. *Gross revenue retention* (GRR) leaves out expansion and can never exceed 100%. *Negative net churn* is another name for NRR above 100%: expansion revenue from existing customers is larger than the revenue lost from cancellations and downgrades.

### Analogy

NRR is like a garden that loses some plants every season while the remaining plants grow larger. If growth of the survivors outweighs the losses, the garden gets fuller without planting anything new.

### Mechanism

NRR works through *land and expand*: accounts start small and add seats, usage or features. It is strongest in business software priced by seat or usage. Practitioners often treat NRR above 100% as healthy and above 120% as excellent for enterprise software; consumer subscriptions rarely exceed 100%, because individuals do not add seats. These are rules of thumb.

Negative net churn is called the holy grail of subscription businesses because growth compounds: new customers add to a base that already grows by itself.

The bridge from starting to current revenue for one cohort:

```mermaid
flowchart LR
  S[Starting MRR 100,000] --> E[+ Expansion 25,000]
  E --> C[- Contraction 4,000]
  C --> CH[- Churn 9,000]
  CH --> X[Current MRR 112,000]
  X --> N[NRR 112%]
```

## Worked example

A cohort of accounts started the year at 100,000 MRR. During the year they added 25,000 in expansion, lost 4,000 to downgrades and 9,000 to cancellations. NRR = (100,000 + 25,000 - 4,000 - 9,000) / 100,000 = 112%. Gross revenue retention = (100,000 - 4,000 - 9,000) / 100,000 = 87%. Even with 13% gross losses, the cohort grew 12%.

## Trade offs and when to use it

NRR summarizes the health of the installed base in one number. It can hide high churn behind strong expansion from a few large accounts, so read it with GRR and with churn by segment.

## Common mistakes

- **Including new customers.** NRR is calculated only for customers active at the start.
- **Reporting NRR without GRR.** Show both, so expansion cannot hide churn.

## Practice

1. Starting MRR 50,000; expansion 8,000; contraction 2,000; churn 3,000. Calculate NRR and GRR.
2. What does negative net churn mean?

### Answers

1. NRR = 53,000 / 50,000 = 106%. GRR = 45,000 / 50,000 = 90%.
2. Expansion from existing customers exceeds revenue lost from cancellations and downgrades.

## Further reading

- Skok, D. (2013). SaaS Metrics 2.0: A guide to measuring and improving what matters. For Entrepreneurs. [Link](https://www.forentrepreneurs.com/saas-metrics-2/). Negative churn and its effect.
- Bessemer Venture Partners. State of the Cloud and cloud benchmarks. Bessemer Venture Partners. [Link](https://www.bvp.com/atlas). Retention benchmarks for cloud companies.
