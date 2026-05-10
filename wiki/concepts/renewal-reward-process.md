---
type: concept
tags: [stochastic-processes, renewal-process, regenerative-processes]
sources: [lecture-notes-ch5, lecture-notes-ch6]
related: [renewal-process, regenerative-process, gobackn-protocol]
---

# Renewal Reward Process

**A renewal reward process accumulates a reward during each renewal cycle and converts cycle averages into long-run rates.**

## Definition

For renewal count $N(t)$ and i.i.d. cycle rewards $R_n$,
$$
R(t)=\sum_{n=1}^{N(t)}R_n.
$$

## Key Properties

- If $\mathbb{E}[R]$ and $\mathbb{E}[X]$ are finite,
$$
\frac{R(t)}{t}\to\frac{\mathbb{E}[R]}{\mathbb{E}[X]}
$$
almost surely, and the expectation version also holds under the source theorem.
- Ratios of two accumulated rewards converge to ratios of their one-cycle expectations.
- Time spent in a state can be treated as a reward.

## Intuition

A long run contains many cycles; total reward divided by total time is reward per cycle divided by time per cycle.

## Connection to Other Concepts

- [[regenerative-process]] uses renewal rewards for time averages.
- [[semi-markov-process]] uses reward/time formulas for state probabilities.
- [[gobackn-protocol]] uses reward/time throughput.

## Theorems

- [[renewal-reward-theorem]]
- [[semi-markov-long-run-distribution]]
- [[gobackn-throughput-markov-errors]]

## Examples

- [[loss-system-poisson-arrivals]]
- [[gobackn-transform-throughput]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch5]] - theorem and regenerative use.
- [[sources/lecture-notes-ch6]] - throughput application.

