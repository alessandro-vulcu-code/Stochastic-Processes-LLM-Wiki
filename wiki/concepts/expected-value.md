---
type: concept
tags: [stochastic-processes, probability, moments]
sources: [lecture-notes-ch1, lecture-notes-ch5]
related: [[concepts/random-variable]], [[concepts/renewal-reward-process]], [[concepts/renewal-function]]
---

# Expected Value

**Expected value is the probability-weighted average of a random variable.**

## Definition

For a discrete random variable $X$,
$$
\mathbb{E}[X]=\sum_x x\,\mathbb{P}(X=x).
$$
For a continuous random variable with density $f_X$,
$$
\mathbb{E}[X]=\int_{-\infty}^{\infty}x f_X(x)\,dx.
$$

## Key Properties

- Linearity: $\mathbb{E}[aX+bY]=a\mathbb{E}[X]+b\mathbb{E}[Y]$.
- Conditional decomposition: $\mathbb{E}[X]=\mathbb{E}[\mathbb{E}[X\mid Y]]$.
- Renewal theory often computes long-run rates by ratios of expectations per cycle.

## Intuition

Expected value is not necessarily the most likely value. It is the balancing point of the distribution and the natural quantity for average cost, waiting time, reward, and renewal count.

## Connection to Other Concepts

The [[concepts/renewal-function|Renewal Function]] is $M(t)=\mathbb{E}[N(t)]$. The [[concepts/renewal-reward-process|Renewal Reward Process]] converts cycle expectations into long-run time averages.

## Theorems

- [[theorems/law-of-total-variance|Law of Total Variance]]
- [[theorems/renewal-reward-theorem|Renewal Reward Theorem]]

## Examples

- If $X(t)$ is Poisson with rate $\lambda t$, then $\mathbb{E}[X(t)]=\lambda t$.
- If $S_i$ are renewal interarrival times with mean $\mu$, then $M(t)/t\to 1/\mu$ under the elementary renewal theorem.

## Open Questions / Gaps

> [!todo] Gap - Add a page for conditional expectation when martingales appear.

## Sources

- [[sources/lecture-notes-ch1]] - moment and conditioning identities.
- [[sources/lecture-notes-ch5]] - renewal counts and reward averages.
