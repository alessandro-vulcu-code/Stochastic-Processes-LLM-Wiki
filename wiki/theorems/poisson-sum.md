---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-distribution]
---

# Sum of Independent Poisson Variables

**The sum of independent Poisson variables is Poisson with parameter equal to the sum of parameters.**

## Statement (Formal)

If $X\sim\mathrm{Poisson}(\mu)$ and $Y\sim\mathrm{Poisson}(\nu)$ are independent, then
$$
X+Y\sim\mathrm{Poisson}(\mu+\nu).
$$

## Proof Sketch

Compute $\mathbb{P}[X+Y=n]$ by summing $\mathbb{P}[X=k]\mathbb{P}[Y=n-k]$ over $k$, then recognize the binomial expansion of $(\mu+\nu)^n$.

## Conditions

Independence is essential.

## Consequences

Supports the superposition theorem for Poisson processes.

## Related Theorems

- [[superposition-theorem]]

## Sources

- [[sources/lecture-notes-ch4]]

