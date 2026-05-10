---
type: concept
tags: [stochastic-processes, distributions, discrete]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [binomial-distribution, poisson-distribution]
---

# Bernoulli Distribution

**The Bernoulli distribution models a single success/failure trial.**

## Definition

A random variable $X\in\{0,1\}$ is Bernoulli with parameter $p$ if
$$
\mathbb{P}[X=1]=p,\qquad \mathbb{P}[X=0]=1-p.
$$
Then
$$
\mathbb{E}[X]=p,\qquad \mathrm{Var}(X)=p(1-p).
$$

## Key Properties

- Indicator variables $\mathbb{1}_A$ are Bernoulli with parameter $\mathbb{P}[A]$.
- Sums of independent Bernoulli variables with common parameter are Binomial.
- Sums of many rare Bernoulli variables are approximately Poisson.

## Intuition

A Bernoulli random variable is the numerical version of a yes/no event.

## Connection to Other Concepts

- [[binomial-distribution]] is a sum of Bernoulli trials.
- [[poisson-distribution]] appears as a rare-event Bernoulli-sum limit.

## Theorems

- [[poisson-limit-theorem]]
- [[poisson-approximation-bound]]

## Examples

- Success indicator for a packet transmission.
- Indicator $\mathbb{1}\{X_m=0\}$ used in Chapter 6 counting distributions.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch1]] - definition, mean, and variance.
- [[sources/lecture-notes-ch4]] - Bernoulli sums in the law of rare events.

