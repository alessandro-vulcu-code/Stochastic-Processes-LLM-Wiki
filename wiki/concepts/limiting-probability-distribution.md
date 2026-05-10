---
type: concept
tags: [stochastic-processes, markov-chains, ergodic-theory]
sources: [lecture-notes-ch3]
related: [[concepts/stationary-distribution]], [[concepts/n-step-transition-probability]], [[concepts/aperiodic]]
---

# Limiting Probability Distribution

**A limiting probability distribution is the pointwise long-run limit of transition probabilities.**

## Definition

For a Markov chain, a limiting distribution is a vector $\pi$ such that
$$
\lim_{n\to\infty}P_{ij}^{(n)}=\pi_j
$$
for relevant starting states $i$.

## Key Properties

- If the limit exists and is independent of $i$, then $\pi$ is stationary.
- A stationary distribution need not be a limiting distribution when the chain is periodic.
- Positive recurrence plus aperiodicity is the key Ch3 condition making the stationary law a limiting law.

## Intuition

The limiting distribution describes what a long-run observer sees at a large time, after transient dependence on the initial state has vanished.

## Connection to Other Concepts

It is related but not identical to [[concepts/stationary-distribution|Stationary Distribution]]. The theorem connecting them is [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]].

## Theorems

- [[theorems/limiting-distribution-regular-markov-chain|Limiting Distribution of a Regular Markov Chain]]
- [[theorems/basic-limit-theorem|Basic Limit Theorem]]
- [[theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]]

## Examples

- A regular finite chain has a unique limiting distribution.
- The deterministic two-state periodic chain has stationary distribution $(1/2,1/2)$ but no ordinary limiting distribution.

## Open Questions / Gaps

> [!todo] Gap - Add Cesaro limiting distribution for periodic chains.

## Sources

- [[sources/lecture-notes-ch3]] - limiting probabilities and stationarity.
