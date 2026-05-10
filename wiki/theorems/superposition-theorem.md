---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-process, poisson-sum]
---

# Superposition Theorem

**The sum of independent Poisson processes is a Poisson process with summed rate.**

## Statement (Formal)

If $X_1(t)$ and $X_2(t)$ are independent Poisson processes with rates $\lambda_1$ and $\lambda_2$, then
$$
X(t)=X_1(t)+X_2(t)
$$
is a Poisson process with rate $\lambda_1+\lambda_2$.

## Proof Sketch

Check $X(0)=0$, independent stationary increments, and Poisson-distributed increments. The increment distribution follows from the sum-of-Poisson theorem.

## Conditions

The processes must be independent.

## Consequences

Multiple independent arrival streams can be modeled as one Poisson stream with total rate.

## Related Theorems

- [[poisson-sum]]
- [[thinning-theorem]]

## Sources

- [[sources/lecture-notes-ch4]]

