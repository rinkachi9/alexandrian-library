# Decision making

## Summary

A decision is a choice among options under uncertainty, and good decision making is about the quality of the process more than the outcome. Real decisions are made with limited time and information, so people satisfice: they accept an option that is good enough. Intuition works well in regular environments with fast feedback, and poorly elsewhere. Tools such as decision trees, expected value and data-driven checks help, and the main practical gain comes from making the criteria and assumptions explicit.

*This note is educational. It is not advice for any specific decision.*

## Prerequisites

- [Heuristics and cognitive biases](../../../../social-sciences/psychology/cognitive-psychology/heuristics-and-biases.md).

## Core concepts

### Definition

*Decision making* is the process of identifying options and choosing among them. Simon (1955) proposed *bounded rationality*: people have limited information and time, so they use simplified procedures and *satisfice*, which means accepting the first option that meets a threshold, instead of maximizing. Kahneman and Klein (2009) argue that expert intuition can be trusted when the environment is regular enough to be learned and the expert had a chance to learn it through practice with feedback, such as in chess or firefighting. In domains with weak feedback, such as long-term forecasts, confidence is not a sign of validity.

### Analogy

Decision making is like packing for a trip with an uncertain forecast: list what you might need, estimate the odds and the cost of each item being missing, and carry what protects against the worst. The limit of the analogy is that the forecast is rarely stated as a probability.

### Process

```mermaid
flowchart LR
  P[Frame the decision] --> O[List options]
  O --> C[Set criteria and weights]
  C --> E[Evaluate: evidence, risks, values]
  E --> D[Decide]
  D --> R[Record reasons and review later]
```

### Styles and tools

| Approach | Use when |
| --- | --- |
| Intuition | Regular domain, fast feedback, experienced decision maker |
| Weighted criteria | Several attributes to compare |
| Expected value | Probabilities and payoffs can be estimated |
| Decision tree | A sequence of choices and uncertain events |
| Data-driven | Relevant data exists and is reliable: define the question, collect, analyze, test and decide |

Milkman, Chugh and Bazerman (2009) review ways to improve decisions: considering the opposite, outside views, taking an advisor's perspective and changing the structure of choice. Data-driven decision making needs clear metrics (key performance indicators), data quality checks and awareness that data answer the question asked and not the one intended.

### Decision trees

A decision tree has decision nodes (choices), chance nodes (uncertain events with probabilities) and end nodes (payoffs). The value of a choice is found by working backward from the payoffs, multiplying by probabilities.

## Worked example

A company can launch a product now, or run a pilot first. Amounts are in thousands and are illustrative: launch costs 100; a successful launch earns 400 and a weak one 50. Without a pilot, P(success) is 0.4. A pilot costs 20, has a 50% chance of being good, and a good pilot lifts P(success) to 0.7. After a bad pilot the company stops.

```python
# Python 3.12. Expected value of a small decision tree (amounts in thousands, illustrative).
def launch_value(p_success):
    return p_success * 400 + (1 - p_success) * 50 - 100      # revenue if success / if weak, minus launch cost

ev_launch_now = launch_value(0.4)
ev_pilot = -20 + 0.5 * launch_value(0.7) + 0.5 * 0           # pilot costs 20; a good pilot lifts P(success) to 0.7; a bad one means stop
print("launch now:", round(ev_launch_now, 1))
print("pilot first:", round(ev_pilot, 1))
print("best:", "launch now" if ev_launch_now > ev_pilot else "pilot first")
```

Output:

```text
launch now: 90.0
pilot first: 77.5
best: launch now
```

Launching now has the higher expected value (90 against 77.5), because the pilot costs 20 and the chance of stopping a bad launch is worth less than that. If a pilot were cheaper or the launch cost larger, the pilot would win. The example shows how making assumptions explicit allows a check of the sensitivity of the answer.

## Trade offs and when to use it

Formal methods help with complex, high-stakes and repeated decisions, and they cost time. Expected value ignores risk attitude, and the probabilities are often guesses. A good practice is to record the reasons and the expected result before the outcome, so that review is fair (see [hindsight bias](../../../../social-sciences/psychology/cognitive-psychology/hindsight-bias.md)).

## Common mistakes

- **Judging decisions by outcomes.** Judge by the information available at the time.
- **Trusting confident intuition in low-feedback domains.** Confidence is not validity.
- **Treating a precise number as an accurate one.** Probabilities are estimates.
- **Not recording reasons.** Review then depends on biased memory.

## Practice

1. What does satisficing mean?
2. When can intuition be trusted, according to Kahneman and Klein (2009)?
3. How is a decision tree evaluated?

### Answers

1. Accepting the first option that meets a threshold instead of seeking the best one.
2. In a regular environment where the person has had practice with fast feedback.
3. Work backward from the payoffs, multiplying by probabilities at chance nodes and choosing the best option at decision nodes.

## Further reading

- Simon, H. A. (1955). A Behavioral Model of Rational Choice. *The Quarterly Journal of Economics*, 69(1), 99. [DOI](https://doi.org/10.2307/1884852). Introduces bounded rationality and satisficing.
- Kahneman, D. and Klein, G. (2009). Conditions for intuitive expertise: A failure to disagree. *American Psychologist*, 64(6), 515-526. [DOI](https://doi.org/10.1037/a0016755). Conditions under which intuitive judgment can be trusted.
- Milkman, K. L., Chugh, D. and Bazerman, M. H. (2009). How Can Decision Making Be Improved?. *Perspectives on Psychological Science*, 4(4), 379-383. [DOI](https://doi.org/10.1111/j.1745-6924.2009.01142.x). Reviews ways of improving decision making.
- Kahneman, D. (2011). *Thinking, Fast and Slow*. Farrar, Straus and Giroux. A general account of heuristics, biases and the two modes of thinking.
