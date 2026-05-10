---
type: theorem
tags: [theorem, probability]
sources: [lecture-notes-ch1]
related: [conditional-probability]
---

# Law of Total Probability

**A probability can be computed by decomposing over a disjoint exhaustive partition.**

## Statement (Formal)

Let $\{A_i\}$ be a disjoint partition of $\Omega$. For any event $B$,
$$
\mathbb{P}[B]=\sum_i\mathbb{P}[B\cap A_i].
$$
Equivalently, when $\mathbb{P}[A_i]>0$,
$$
\mathbb{P}[B]=\sum_i\mathbb{P}[B\mid A_i]\mathbb{P}[A_i].
$$

## Proof Sketch

The sets $B\cap A_i$ are disjoint and their union is $B$. Additivity of probability gives the result.

## Conditions

The $A_i$ must be mutually disjoint and exhaustive.

## Consequences

This is the basic marginalization tool behind conditioning, first-step analysis, and random-sum computations.

## Related Theorems

- [[law-of-total-variance]]

## Sources

- [[sources/lecture-notes-ch1]]

