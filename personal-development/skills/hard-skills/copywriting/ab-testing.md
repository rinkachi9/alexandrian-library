# A/B testing

## Summary

An A/B test, or online controlled experiment, randomly splits visitors between two versions of a page, email or ad and compares a chosen metric, such as the share of visitors who buy. Because the split is random, a difference larger than chance can be attributed to the change itself and not to the season, the traffic source or luck. The method is simple, but trustworthy results need a metric chosen in advance, enough visitors, a fixed stopping rule and checks that the split worked. Without enough traffic, small changes cannot be tested at all.

## Prerequisites

Basic ideas of probability and sampling. The marketing uses of tests are in [headlines](../content-marketing/headlines.md) and [calls to action and risk reversal](calls-to-action-and-risk-reversal.md).

## Core concepts

### Definition

An *A/B test* is a randomized controlled experiment in which each unit (usually a visitor or a user) is assigned at random to a *control* (A, the current version) or a *treatment* (B, the changed version), and a predefined *metric* is compared between the groups. Tests with more than two versions are called A/B/n tests. The term *online controlled experiment* is used in the research literature.

*Analogy.* An A/B test works like a clinical trial for a web page. Patients are assigned at random to the new drug or the old one, so that age, health and luck are spread evenly, and any difference in outcomes can be credited to the drug. The analogy breaks in one direction: a web test can reach thousands of people in days and change nothing about their health, so it is cheap to repeat. It also breaks in another: people online may see both versions on different devices, which a clinical trial carefully prevents.

### The problem it solves

Before controlled experiments, marketers compared periods ("conversion went up after we changed the button"). Many things change between periods: the season, competitors, ad campaigns, the mix of visitors. Randomization removes those differences on average, so the comparison is fair. It also protects against the opinion of the most senior person in the room, which is often wrong. Kohavi, Tang and Xu report from experience at Microsoft, Google and LinkedIn that most ideas tested do not improve the metric they target.

### Mechanism

1. **Hypothesis.** "Showing the guarantee inside the button area will raise purchases, because buyers worry about risk."
2. **Metric.** One primary metric decided before the test, such as purchases per visitor. Add *guardrail* metrics that must not get worse, such as refund rate or page load time.
3. **Randomization unit.** Usually the user, so that a person sees the same version on every visit.
4. **Sample size.** Calculated before the test from the baseline rate and the smallest effect worth detecting (below).
5. **Run.** Split traffic, for example 50/50, for at least one full week to cover weekday patterns.
6. **Checks.** Verify that the groups received the planned share of traffic. A *sample ratio mismatch* (for example 52/48 when 50/50 was planned, with large samples) means something in the setup is broken, and the result should not be trusted.
7. **Analysis.** Compare the metric with a statistical test. A *p-value* below the chosen threshold (commonly 0.05) means a difference this large would be unlikely if the change had no effect.
8. **Decision.** Ship, drop or iterate. Record the result.

### Sample size

The number of visitors needed depends on the baseline rate and the smallest difference you want to detect. A common approximation for 80% power and a 5% significance level is:

n per group ≈ 16 × σ² / δ²

where σ² is the variance of the metric (for a conversion rate p, σ² = p(1 - p)) and δ is the absolute difference to detect. Kohavi, Tang and Xu use this rule of thumb.

```python
# Python 3.13. Sample size per group for a conversion-rate A/B test.
p = 0.03                 # baseline conversion rate: 3%
relative_lift = 0.10     # smallest effect worth detecting: 10% relative
delta = p * relative_lift
variance = p * (1 - p)
n = 16 * variance / delta**2
print(round(n))
```

Output:

```text
51733
```

So detecting a change from 3.0% to 3.3% needs about 52,000 visitors per version, about 104,000 in total. A site with 2,000 visitors a week would need about a year. Small sites should test only large changes or use other evidence.

### Peeking

*Peeking* means checking the result repeatedly and stopping as soon as it looks significant. Each look is another chance for noise to cross the threshold, so the real false positive rate becomes much higher than 5%. Fix the sample size in advance, or use a method designed for continuous monitoring (sequential testing), which many testing tools offer.

### What can be tested

Headlines and email subject lines, CTA wording and placement, guarantee wording, prices and offers, page layout, images, the order of steps in a checkout. Prices need care: in the EU, showing different prices to different consumers can raise legal and fairness questions, and personalized pricing based on automated decision making must be disclosed (Consumer Rights Directive as amended by Directive 2019/2161).

## Worked example

An email newsletter with 40,000 subscribers tests two subject lines for the same issue.

- A: "This month's gardening tips"
- B: "The 3 plants to sow before the first frost"

Each version goes to 20,000 randomly chosen subscribers. Primary metric: click rate on the article link (opens are less reliable because some email clients load images automatically). Guardrail: unsubscribe rate.

Results (invented): A gets 600 clicks (3.0%), B gets 720 clicks (3.6%). A two-proportion z-test gives z ≈ 3.36 and a p-value of about 0.0008 (computed with Python 3.13), and the unsubscribe rates are equal. The team adopts specific, benefit-led subject lines for future issues and keeps testing, because one result on one issue does not prove a general rule.

## Trade offs and when to use it

- **Best for causal questions with enough traffic.** It answers "does B work better than A for these users now?"
- **Not suited to small samples,** rare events or long-term effects that appear after months.
- **Short-term metrics can mislead.** A pushy design can raise purchases this week and returns next month. Use guardrails and look at longer horizons.
- **Novelty effects.** Users may click a new design because it is new. Run tests long enough for the effect to settle.
- **Cost.** Tooling, analysis time and the risk of showing a worse version to half the users.

## Common mistakes

- **Choosing the metric after seeing the results.** Fix: write the hypothesis and metric down before starting.
- **Stopping as soon as the result looks good.** Fix: fixed sample size or a sequential method.
- **Ignoring sample ratio mismatch.** Fix: check the split before reading the results.
- **Testing many metrics and reporting the one that moved.** Fix: one primary metric, correction for multiple comparisons on the rest.
- **Generalizing one test to all situations.** Fix: repeat important tests and treat results as local.

## Practice

1. Why does randomization make an A/B comparison fairer than a before and after comparison?
2. Calculate the sample size per group to detect a change from 5% to 6% conversion with the rule of thumb.
3. What is a sample ratio mismatch, and what should you do when you see one?
4. Why is peeking a problem?

Hints: for question 2, δ = 0.01 and σ² = 0.05 × 0.95. The answer is 7,600 per group.

## Further reading

- Kohavi, R., Tang, D., & Xu, Y. (2020). *Trustworthy Online Controlled Experiments: A Practical Guide to A/B Testing*. Cambridge University Press. [doi:10.1017/9781108653985](https://doi.org/10.1017/9781108653985). The standard practical reference, including sample ratio mismatch.
- Fabijan, A., et al. (2019). Diagnosing sample ratio mismatch in online controlled experiments. *Proceedings of the 25th ACM SIGKDD Conference*. [doi:10.1145/3292500.3330722](https://doi.org/10.1145/3292500.3330722). How to detect and diagnose a broken split.

TODO: Confirm in the Kohavi et al. book the statement that most tested ideas fail to improve their metric, and the chapter numbers for peeking and the 16σ²/δ² rule. Verify the author list and DOI of Fabijan et al. (2019).
