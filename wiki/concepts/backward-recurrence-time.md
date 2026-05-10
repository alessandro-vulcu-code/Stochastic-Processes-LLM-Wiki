---
type: concept
tags: [stochastic-processes, renewal-process, poisson-process]
sources: [lecture-notes-ch4, lecture-notes-ch5]
related: [[concepts/excess-life]], [[concepts/renewal-process]], [[concepts/sampling-paradox]]
---

# Backward Recurrence Time

**The backward recurrence time is the age of the current renewal interval at observation time $t$.**

## Definition

For a renewal process with renewal epochs $S_n$, the backward recurrence time at time $t$ is
$$
\delta_t=t-S_{N(t)}.
$$
It measures how long it has been since the last renewal before $t$.

## Key Properties

- It is paired with [[concepts/excess-life|Excess Life]], $\gamma_t=S_{N(t)+1}-t$.
- In a Poisson process, memorylessness makes forward and backward views especially tractable.
- In general renewal processes, asymptotic age and residual-life distributions are biased toward longer intervals.

## Intuition

If you arrive at a random time, you are more likely to land in a long interval than a short one. The backward time records how far into that interval you are.

## Connection to Other Concepts

Backward recurrence time is central to the [[concepts/sampling-paradox|Sampling Paradox]] and stationary renewal constructions.

## Theorems

- [[theorems/basic-renewal-theorem|Basic Renewal Theorem]]

## Examples

- In the Poisson case, past and future are independent because disjoint increments are independent.

## Open Questions / Gaps

> [!todo] Gap - Add exact limiting density formulas for age and excess life.

## Sources

- [[sources/lecture-notes-ch4]] - Poisson-process backward/forward conditioning examples.
- [[sources/lecture-notes-ch5]] - renewal age and excess-life discussion.
