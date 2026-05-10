---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3, lecture-notes-ch5]
related: [[concepts/recurrence]], [[concepts/null-recurrent]], [[concepts/stationary-distribution]]
---

# Positive Recurrent

**A recurrent state is positive recurrent when its expected return time is finite.**

## Definition

For a recurrent state $i$, let $m_i=\mathbb{E}[R_i\mid X_0=i]$ be the mean return time to $i$. State $i$ is positive recurrent if
$$
m_i<\infty.
$$

## Key Properties

- Positive recurrence is a class property.
- In an irreducible positive recurrent aperiodic class, $\pi_i=1/m_i$ and $P_{ji}^{(n)}\to\pi_i$.
- Finite irreducible recurrent classes are positive recurrent.

## Intuition

The chain returns not only with probability one, but quickly enough on average to spend a positive fraction of time in the state.

## Connection to Other Concepts

Positive recurrence sits between [[concepts/recurrence|Recurrence]] and [[concepts/stationary-distribution|Stationary Distribution]]: it is the recurrence condition that supports a normalized invariant law.

## Theorems

- [[theorems/basic-limit-theorem|Basic Limit Theorem]]
- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]
- [[theorems/finite-state-positive-recurrence|Finite-State Positive Recurrence Facts]]

## Examples

- The M/G/1 embedded queue is positive recurrent when traffic intensity $\rho<1$.

## Open Questions / Gaps

> [!todo] Gap - Add Foster-Lyapunov criteria if later sources cover them.

## Sources

- [[sources/lecture-notes-ch3]] - classification and stationarity equations.
- [[sources/lecture-notes-ch5]] - renewal proof of $\pi_i=1/m_i$.
