---
type: theorem
tags: [theorem, probability, poisson-process]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [poisson-distribution]
---

# Poisson Limit Theorem

**A Binomial count with many trials and rare successes converges to a Poisson distribution.**

## Statement (Formal)

If $X_n\sim\mathrm{Binomial}(n,p_n)$ with $np_n\to\lambda$, then
$$
\mathbb{P}[X_n=k]\to \frac{\lambda^k e^{-\lambda}}{k!}.
$$

## Proof Sketch

Write the Binomial mass and use $p_n\sim\lambda/n$, $(1-\lambda/n)^n\to e^{-\lambda}$, and the finite-$k$ limit of the combinatorial factor.

## Conditions

$k$ is fixed while $n\to\infty$ and individual success probabilities vanish.

## Consequences

This is the distribution-level form of the law of rare events.

## Related Theorems

- [[poisson-approximation-bound]]

## Sources

- [[sources/lecture-notes-ch1]]
- [[sources/lecture-notes-ch4]]

