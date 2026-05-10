---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-process, poisson-binomial-filter]
---

# Thinning Theorem

**Independent marking of Poisson arrivals splits one Poisson process into independent Poisson subprocesses.**

## Statement (Formal)

Let $X(t)$ be Poisson with rate $\lambda$. Mark each arrival as type 1 with probability $p$ and type 2 with probability $1-p$, independently. Then the type-counting processes are independent Poisson processes with rates $\lambda p$ and $\lambda(1-p)$.

## Proof Sketch

Condition on the total count, use the binomial distribution for type assignments, and simplify the joint mass into a product of two Poisson masses.

## Conditions

Marking must be independent across arrivals and independent of the process.

## Consequences

Models independent routing, filtering, or classification of Poisson arrivals.

## Related Theorems

- [[poisson-binomial-filter]]
- [[superposition-theorem]]

## Sources

- [[sources/lecture-notes-ch4]]

