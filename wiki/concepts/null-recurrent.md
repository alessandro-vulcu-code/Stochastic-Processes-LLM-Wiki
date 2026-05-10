---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[concepts/recurrence]], [[concepts/positive-recurrent]], [[concepts/state-classification]]
---

# Null Recurrent

**A recurrent state is null recurrent when it returns almost surely but with infinite mean return time.**

## Definition

State $i$ is null recurrent if it is recurrent and
$$
m_i=\mathbb{E}[R_i\mid X_0=i]=\infty.
$$

## Key Properties

- Null recurrence is a class property.
- A null recurrent state is visited infinitely often with probability one but has zero long-run occupation fraction.
- Finite-state chains cannot contain null recurrent states.

## Intuition

The chain always comes back, but return times are so heavy-tailed that no positive limiting mass remains at the state.

## Connection to Other Concepts

Null recurrence contrasts with [[concepts/positive-recurrent|Positive Recurrent]] and is one possible outcome in [[concepts/state-classification|State Classification]].

## Theorems

- [[theorems/finite-state-positive-recurrence|Finite-State Positive Recurrence Facts]]
- [[theorems/recurrence-criterion|Recurrence Criterion]]

## Examples

- The critical M/G/1 embedded chain in the notes is null recurrent at $\rho=1$.

## Open Questions / Gaps

> [!todo] Gap - Add standard random-walk examples such as simple symmetric walk on $\mathbb{Z}$.

## Sources

- [[sources/lecture-notes-ch3]] - recurrence classification and queue examples.
