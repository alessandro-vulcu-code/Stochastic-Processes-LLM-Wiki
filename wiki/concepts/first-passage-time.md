---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [first-step-analysis, recurrence]
---

# First Passage Time

**The first passage time $\theta_{ij}$ is the number of transitions needed to reach state $j$ from state $i$ for the first time.**

## Definition

For $i\neq j$,
$$
\theta_{ij}=\min\{n\geq 1:X_n=j\mid X_0=i\}.
$$
Its distribution is
$$
f_{ij}(n)=\mathbb{P}[X_n=j,\ X_m\neq j,\ m=1,\ldots,n-1\mid X_0=i].
$$

## Key Properties

- First-passage distributions satisfy first-step recursions.
- First return times $\theta_{ii}$ determine recurrence and mean return time.
- Mean first-passage times satisfy linear equations.

## Intuition

First passage ignores all paths that hit the target earlier; it records the first successful arrival.

## Connection to Other Concepts

- [[recurrence]] is defined by return probabilities.
- [[first-step-analysis]] computes first-passage probabilities and means.
- [[basic-limit-theorem]] uses mean return times.

## Theorems

- [[mean-first-passage-time]]
- [[basic-limit-theorem]]

## Examples

- Two-state chain first passage has geometric form.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch2]] - first-passage recursion and mean equations.
- [[sources/lecture-notes-ch3]] - first return and recurrence.

