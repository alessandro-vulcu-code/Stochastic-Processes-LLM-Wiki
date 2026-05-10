---
type: concept
tags: [stochastic-processes, distributions, continuous, poisson-process]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [exponential-distribution, poisson-process]
---

# Gamma Distribution

**The gamma distribution gives the sum of independent exponential waiting times, including the time of the $n$-th Poisson arrival.**

## Definition

With shape $\alpha>0$ and rate $\lambda>0$,
$$
f(x)=\frac{\lambda}{\Gamma(\alpha)}(\lambda x)^{\alpha-1}e^{-\lambda x},\qquad x>0.
$$
For integer $\alpha=n$, it is the sum of $n$ i.i.d. Exp$(\lambda)$ variables.

## Key Properties

- Mean $\alpha/\lambda$.
- Variance $\alpha/\lambda^2$.
- In a Poisson process, $W_n\sim\mathrm{Gamma}(n,\lambda)$.

## Intuition

Waiting for the $n$-th event is the sum of $n$ independent waits for the next event.

## Connection to Other Concepts

- [[exponential-distribution]] is the $\alpha=1$ case.
- [[poisson-process]] waiting times are gamma-distributed.

## Theorems

- [[waiting-times-gamma]]

## Examples

- [[geometric-sum-exponentials]] uses gamma mixtures.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch1]] - definition and moments.
- [[sources/lecture-notes-ch4]] - waiting-time result.

