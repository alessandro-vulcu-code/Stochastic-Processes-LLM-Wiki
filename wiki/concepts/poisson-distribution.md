---
type: concept
tags: [stochastic-processes, distributions, poisson-process]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [poisson-process, poisson-limit-theorem]
---

# Poisson Distribution

**The Poisson distribution models counts of rare independent events with rate parameter $\lambda$.**

## Definition

For $\lambda>0$,
$$
\mathbb{P}[X=k]=\frac{\lambda^k e^{-\lambda}}{k!},\qquad k=0,1,2,\ldots.
$$
It satisfies
$$
\mathbb{E}[X]=\mathrm{Var}(X)=\lambda.
$$

## Key Properties

- Limit of Binomial$(n,\lambda/n)$ as $n\to\infty$.
- Sum of independent Poisson variables is Poisson with summed parameters.
- Independent Bernoulli thinning of a Poisson variable preserves the Poisson form with scaled rate.

## Intuition

The parameter is both the expected count and the count variance. Independent sources add rates.

## Connection to Other Concepts

- [[poisson-process]] has increments distributed as Poisson$(\lambda t)$.
- [[thinning-theorem]] and [[superposition-theorem]] are process-level analogues of distribution-level facts.

## Theorems

- [[poisson-limit-theorem]]
- [[poisson-sum]]
- [[poisson-binomial-filter]]
- [[poisson-approximation-bound]]

## Examples

- Number of events in a fixed interval for a Poisson process.
- Retained arrivals after independent filtering.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch1]] - definition, moments, rare-event limit.
- [[sources/lecture-notes-ch4]] - closure properties and approximation bound.

