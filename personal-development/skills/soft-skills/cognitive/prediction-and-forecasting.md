# Prediction and forecasting

## Summary

Forecasting is estimating the probability of future events. Research by Philip Tetlock and colleagues shows that most experts forecast little better than simple baselines, and that some people, called superforecasters, are consistently more accurate. Their habits can be learned: break questions into parts, start from base rates, use probabilities and update in small steps. Forecasts are judged with scoring rules such as the Brier score, which rewards both calibration and the willingness to commit to a probability.

*This note is educational.*

## Prerequisites

- [Decision making](decision-making.md).

## Core concepts

### Definition

A *forecast* is a statement about the probability that an event will occur by a given time. *Calibration* means that of all events given 70% probability, about 70% occur. *Resolution* means that forecasts separate events that happen from those that do not. Tetlock and Gardner (2015) describe the traits of the best forecasters: careful, humble, comfortable with numbers, open to changing their minds and inclined to think in probabilities. Mellers and colleagues (2014) found in a forecasting tournament that training in probabilistic reasoning, working in teams and tracking performance improved accuracy.

### Analogy

Forecasting is like weather prediction: nobody can say whether it will rain, but a forecaster can say 30%, and over many days the rain frequency should match. The limit of the analogy is that weather has a large body of data, while many questions in business and politics have only a few similar cases.

### Methods

```mermaid
flowchart LR
  Q[Question] --> S[Split into parts]
  S --> B[Start from the base rate]
  B --> A[Adjust for specific evidence]
  A --> P[Give a probability]
  P --> U[Update when new evidence arrives]
  U --> R[Score and review]
```

| Habit | Why |
| --- | --- |
| Use base rates | Prevents overweighting a vivid story |
| Use numbers, not words | "Likely" means different things to different people |
| Update in small steps | Avoids overreaction to news |
| Keep score | Gives feedback, which most people never get |
| Consider alternatives | Reduces overconfidence |

Pattern recognition, the other side of prediction, is the ability to see regularities in data and in experience. It is strong in regular environments with feedback, and misleading when people see patterns in noise.

### Scoring with the Brier score

The Brier score (Brier, 1950) is the mean squared difference between the forecast probability and the outcome (1 if it happened, 0 if not). It ranges from 0 (perfect) to 1 (worst), and a constant 50% forecast scores 0.25.

## Worked example

Six forecasts and outcomes.

```python
# Python 3.12. Brier score: mean squared error of probability forecasts (lower is better).
forecasts = [0.9, 0.8, 0.6, 0.3, 0.7, 0.2]
outcomes = [1, 1, 0, 0, 1, 0]            # 1 = the event happened

def brier(f, o):
    return sum((p - x) ** 2 for p, x in zip(f, o)) / len(f)

print("forecaster:", round(brier(forecasts, outcomes), 3))
print("always 50%:", round(brier([0.5] * 6, outcomes), 3))
print("overconfident:", round(brier([1.0 if p >= 0.5 else 0.0 for p in forecasts], outcomes), 3))
```

Output:

```text
forecaster: 0.105
always 50%: 0.25
overconfident: 0.167
```

The forecaster (0.105) beats both the 50% baseline (0.25) and the overconfident version of the same forecasts, rounded to 0 or 1 (0.167). The overconfident forecaster is penalized for the one confident miss on the third question. The sample is only six forecasts, so the comparison is a demonstration and not evidence of skill.

## Trade offs and when to use it

Probabilistic forecasting helps when decisions depend on uncertain events, and when feedback is possible. It does not work for unprecedented events, and gives a false sense of precision when the numbers are guesses. Tracking forecasts over time is the main route to improvement.

## Common mistakes

- **Using vague words.** "Probably" cannot be scored.
- **Giving 0% or 100%.** One surprise ruins the score.
- **Never checking results.** There is then no learning.
- **Seeing patterns in noise.** Check against random data.

## Practice

1. What does calibration mean?
2. What does a Brier score of 0.25 mean for a constant 50% forecast?
3. Name two habits of good forecasters.

### Answers

1. Of the events given a probability p, about the fraction p occur.
2. It is the baseline of a forecaster who says 50% each time, so a useful forecaster should score lower.
3. For example start from base rates and update in small steps.

## Further reading

- Tetlock, P. E. and Gardner, D. (2015). *Superforecasting: The Art and Science of Prediction*. Crown. Describes what makes some forecasters consistently more accurate.
- Mellers, B., Ungar, L., Baron, J. et al. (2014). Psychological Strategies for Winning a Geopolitical Forecasting Tournament. *Psychological Science*, 25(5), 1106-1115. [DOI](https://doi.org/10.1177/0956797614524255). Evidence on what makes forecasters accurate in a tournament.
- Brier, G. W. (1950). VERIFICATION OF FORECASTS EXPRESSED IN TERMS OF PROBABILITY. *Monthly Weather Review*, 78(1), 1-3. [DOI](https://doi.org/10.1175/1520-0493(1950)078<0001:VOFEIT>2.0.CO;2). The original paper on the Brier score for probability forecasts.
