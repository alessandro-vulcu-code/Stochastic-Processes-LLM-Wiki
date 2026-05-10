---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4, lecture-notes-ch1]
related: [poisson-distribution]
---

# Binomial Filter of a Poisson Variable

**Independent Bernoulli filtering of a Poisson count gives another Poisson count with scaled parameter.**

## Statement (Formal)

If $N\sim\mathrm{Poisson}(\mu)$ and, conditional on $N$, $M\mid N\sim\mathrm{Binomial}(N,p)$, then
$$
M\sim\mathrm{Poisson}(\mu p).
$$

## Proof Sketch

Use total probability over $N=n$ and simplify the resulting series by the exponential expansion.

## Conditions

The filtering decisions must be conditionally independent with common probability $p$.

## Consequences

Distribution-level version of Poisson process thinning.

## Related Theorems

- [[thinning-theorem]]

## Sources

- [[sources/lecture-notes-ch4]]
- [[sources/lecture-notes-ch1]]

