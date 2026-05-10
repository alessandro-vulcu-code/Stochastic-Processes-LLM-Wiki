---
type: theorem
tags: [theorem, markov-chains, recurrence, ergodic-theory]
sources: [lecture-notes-ch3]
related: [[concepts/positive-recurrent]], [[concepts/aperiodic]], [[concepts/stationary-distribution]], [[concepts/limiting-probability-distribution]]
---

# Stationary Distribution for a Positive Recurrent Aperiodic Class

**Statement** In a positive recurrent aperiodic class, the limiting probabilities are the unique nonnegative solution of the stationarity equations.

## Statement (Formal)

Let $C$ be a positive recurrent aperiodic communicating class. Then for $i,j\in C$,
$$
\lim_{n\to\infty}P_{ij}^{(n)}=\pi_j,
$$
where $\pi$ is the unique nonnegative normalized solution of
$$
\pi_j=\sum_{i\in C}\pi_iP_{ij},\qquad \sum_{j\in C}\pi_j=1.
$$
Moreover $\pi_j=1/m_j$, where $m_j$ is the mean return time to $j$.

## Proof Sketch

The source derives the result from the basic limit theorem for recurrent irreducible aperiodic chains. Positive recurrence makes $m_j<\infty$, so the limiting mass $1/m_j$ is positive and normalizable. Aperiodicity prevents oscillatory subsequential limits, and stationarity follows by passing to the limit in the transition equations.

## Conditions

- The class must be closed/recurrent when considered by itself.
- Positive recurrence is needed for a normalizable invariant probability.
- Aperiodicity is needed for ordinary limits $P_{ij}^{(n)}$ to exist.

## Consequences

- Solving $\pi=\pi P$ is enough to identify the limiting distribution in this setting.
- If the stationary equations have no normalized solution for an irreducible aperiodic chain, the chain is not positive recurrent.
- Periodic chains may have stationary distributions without ordinary limiting distributions.

## Related Theorems

- [[theorems/basic-limit-theorem|Basic Limit Theorem]]
- [[theorems/stationary-distribution-positive-recurrent-class|Stationary Distribution for a Positive Recurrent Aperiodic Class]]
- [[theorems/basic-limit-theorem-renewal-proof|Basic Limit Theorem via Renewal Theory]]

## Sources

- [[sources/lecture-notes-ch3]] - Theorem 3.4.2.
