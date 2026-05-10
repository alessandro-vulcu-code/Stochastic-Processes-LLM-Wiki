---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [absorbing-markov-chain, recurrence]
---

# Transient-to-Recurrent Limit Theorem

**Long-run probability from a transient state to a recurrent-class state factors into absorption probability times class equilibrium.**

## Statement (Formal)

Let $i$ be transient and $j\in C$, where $C$ is an aperiodic recurrent class. Then
$$
\lim_{n\to\infty}P_{ij}^{(n)}=\pi_i(C)\pi_j,
$$
where $\pi_i(C)$ is the probability of eventual entrance into $C$ from $i$, and $\pi_j$ is the limiting probability of $j$ inside $C$.

## Proof Sketch

Decompose the event $\{X_n=j\}$ by the first time and first state at which the chain enters $C$. After entering $C$, apply the Basic Limit Theorem inside the class.

## Conditions

The recurrent class $C$ must be aperiodic for ordinary limits.

## Consequences

Reducible-chain limits can be computed by absorption probabilities and recurrent-class stationary distributions.

## Related Theorems

- [[basic-limit-theorem]]
- [[absorption-probabilities]]

## Sources

- [[sources/lecture-notes-ch3]]

