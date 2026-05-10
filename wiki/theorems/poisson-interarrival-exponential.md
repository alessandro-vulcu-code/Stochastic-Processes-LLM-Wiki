---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4, lecture-notes-ch2]
related: [poisson-process, exponential-distribution]
---

# Poisson Inter-Arrivals Are Exponential

**The inter-arrival times of a Poisson process are i.i.d. exponential with the process rate.**

## Statement (Formal)

For a Poisson process with rate $\lambda$, the inter-arrival times $S_i$ satisfy
$$
S_i\stackrel{\mathrm{i.i.d.}}{\sim}\mathrm{Exp}(\lambda).
$$

## Proof Sketch

The waiting time exceeds $t$ exactly when no arrival occurs in an interval of length $t$, whose probability is $e^{-\lambda t}$. Independent increments give independence across inter-arrivals.

## Conditions

Uses the independent stationary increment definition of the Poisson process.

## Consequences

Poisson processes are renewal processes with exponential interrenewal times.

## Related Theorems

- [[memoryless-property]]
- [[waiting-times-gamma]]

## Sources

- [[sources/lecture-notes-ch4]]
- [[sources/lecture-notes-ch2]]

