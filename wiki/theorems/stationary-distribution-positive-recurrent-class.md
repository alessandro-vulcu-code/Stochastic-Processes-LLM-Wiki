---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[concepts/stationary-distribution]], [[concepts/positive-recurrent]], [[concepts/aperiodic]], [[theorems/stationary-distribution-positive-recurrent-aperiodic]]
---

# Stationary Distribution for a Positive Recurrent Aperiodic Class

**A positive recurrent aperiodic class has a unique stationary probability distribution equal to its limiting distribution.**

> [!note] Canonical page
> The fuller page for the user-requested Theorem 3.4.2 slug is [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]. This page is kept as an earlier alias because existing links may point here.

## Statement (Formal)

For a positive recurrent aperiodic class,
$$
\pi_j=\sum_i\pi_iP_{ij},\qquad \sum_i\pi_i=1,\qquad \pi_i\geq0.
$$
The limiting probabilities satisfy $\lim_{n\to\infty}P_{ij}^{(n)}=\pi_j$.

## Proof Sketch

Use the Basic Limit Theorem for existence and stationarity. Uniqueness follows by comparing any stationary solution with the limiting probabilities.

## Conditions

Positive recurrence and aperiodicity within an irreducible class.

## Consequences

Stationary equations can be used to compute long-run probabilities even for countable classes when a solution exists.

## Related Theorems

- [[theorems/basic-limit-theorem|Basic Limit Theorem]]
- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]

## Sources

- [[sources/lecture-notes-ch3]]
