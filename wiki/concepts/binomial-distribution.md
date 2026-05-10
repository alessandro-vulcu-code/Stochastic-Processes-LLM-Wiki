---
type: concept
tags: [stochastic-processes, distributions, discrete]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [bernoulli-distribution, poisson-distribution]
---

# Binomial Distribution

**The Binomial distribution counts successes in a fixed number of independent Bernoulli trials.**

## Definition

If $Y$ counts successes in $n$ independent trials with success probability $p$, then
$$
\mathbb{P}[Y=k]=\binom{n}{k}p^k(1-p)^{n-k},\qquad k=0,\ldots,n.
$$
It has
$$
\mathbb{E}[Y]=np,\qquad \mathrm{Var}(Y)=np(1-p).
$$

## Key Properties

- A sum of $n$ i.i.d. Bernoulli$(p)$ variables is Binomial$(n,p)$.
- Consecutive independent thinning operations multiply their keep probabilities.
- In the rare-event scaling $np\to\lambda$, Binomial converges to Poisson.

## Intuition

Binomial counts how many yes/no trials succeed out of a fixed batch.

## Connection to Other Concepts

- [[bernoulli-distribution]] supplies the single trial.
- [[poisson-distribution]] is the rare-event limit.
- [[thinning-theorem]] is the process-level version of binomial filtering.

## Theorems

- [[poisson-limit-theorem]]
- [[poisson-binomial-filter]]
- [[binomial-conditional-distribution]]

## Examples

- [[binomial-poisson-thinning]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch1]] - definition and composition exercises.
- [[sources/lecture-notes-ch4]] - conditional Poisson-arrival counts.

