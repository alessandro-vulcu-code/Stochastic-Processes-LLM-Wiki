---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3, lecture-notes-ch5]
related: [recurrence, stationary-distribution, period]
---

# Basic Limit Theorem

**In a recurrent irreducible aperiodic Markov chain, limiting probabilities equal reciprocals of mean return times.**

## Statement (Formal)

For a recurrent, irreducible, aperiodic Markov chain,
$$
\lim_{n\to\infty}P_{ji}^{(n)}=\pi_i=\frac{1}{m_i},
$$
where
$$
m_i=\sum_{n=1}^{\infty}n f_{ii}^{(n)}.
$$

## Proof Sketch

Chapter 3 states the result and defers the proof. Chapter 5 proves it by observing that visits to state $i$ form a renewal process. The Basic Renewal Theorem applied to the visit-count process gives the asymptotic one-step renewal increment $1/m_i$.

## Conditions

Requires recurrence, irreducibility within the class, and aperiodicity for ordinary limits. Periodic classes require subsequence or Cesaro forms.

## Consequences

Positive recurrence ($m_i<\infty$) gives positive long-run mass. Null recurrence gives $\pi_i=0$ despite certain return.

## Related Theorems

- [[basic-limit-theorem-renewal-proof]]
- [[stationary-distribution-positive-recurrent-class]]

## Sources

- [[sources/lecture-notes-ch3]]
- [[sources/lecture-notes-ch5]]

