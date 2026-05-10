---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-distribution, poisson-limit-theorem]
---

# Poisson Approximation Bound

**The error in approximating a sum of rare Bernoulli variables by a Poisson law is bounded by the sum of squared success probabilities.**

## Statement (Formal)

Let $\epsilon_i$ be independent Bernoulli variables with $\mathbb{P}[\epsilon_i=1]=p_i$ and $S_n=\sum_{i=1}^n\epsilon_i$. With $\mu=\sum_i p_i$,
$$
\left|\mathbb{P}[S_n=k]-\frac{\mu^k e^{-\mu}}{k!}\right|
\leq \sum_{i=1}^n p_i^2.
$$

## Proof Sketch

The source states the bound as the formal quantitative version of the law of rare events.

## Conditions

The Bernoulli variables are independent and individual $p_i$ should be small for the bound to be useful.

## Consequences

Justifies Poisson modeling for aggregate rare events even with heterogeneous probabilities.

## Related Theorems

- [[poisson-limit-theorem]]

## Sources

- [[sources/lecture-notes-ch4]]

