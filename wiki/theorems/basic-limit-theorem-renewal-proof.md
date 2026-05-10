---
type: theorem
tags: [theorem, renewal-process, markov-chains]
sources: [lecture-notes-ch5]
related: [basic-limit-theorem, renewal-process]
---

# Basic Limit Theorem via Renewal Theory

**Visits to a recurrent Markov-chain state form a renewal process, proving the Basic Limit Theorem.**

## Statement (Formal)

For a recurrent irreducible aperiodic Markov chain,
$$
\lim_{n\to\infty}P_{ij}^{(n)}=\pi_j=\frac{1}{m_j}.
$$

## Proof Sketch

Starting from $j$, visits to $j$ are renewals with interrenewal distribution equal to return times. The expected increment $M(n)-M(n-1)$ equals $P_{jj}^{(n)}$, and the Basic Renewal Theorem gives convergence to $1/m_j$. Starting from $i\neq j$ gives a delayed renewal process, which has the same long-run rate.

## Conditions

Recurrence, irreducibility, and aperiodicity for ordinary convergence.

## Consequences

Explains why long-run state probabilities are inverse mean recurrence times.

## Related Theorems

- [[basic-renewal-theorem]]
- [[basic-limit-theorem]]

## Sources

- [[sources/lecture-notes-ch5]]

