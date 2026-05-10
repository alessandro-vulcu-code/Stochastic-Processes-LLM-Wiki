---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [first-passage-time, stationary-distribution, communicating-classes]
---

# Recurrence

**Recurrence classifies whether a Markov chain returns to a state with probability one.**

## Definition

Let
$$
f_{ii}=\sum_{n=1}^{\infty}f_{ii}^{(n)}
$$
be the probability of ever returning to $i$ after starting at $i$.

- $i$ is recurrent if $f_{ii}=1$.
- $i$ is transient if $f_{ii}<1$.
- A recurrent state is positive recurrent if $m_i=\sum_{n\geq1}n f_{ii}^{(n)}<\infty$.
- It is null recurrent if $f_{ii}=1$ and $m_i=\infty$.

## Key Properties

- Recurrence is a class property.
- Positive recurrence gives positive long-run mass.
- Null recurrence returns almost surely but with infinite mean return time.
- Finite-state chains have at least one positive recurrent state and no null recurrent states.

## Intuition

Transient states are visited only finitely often on average; recurrent states keep coming back. Positive recurrence means they come back often enough to occupy nonzero long-run time.

## Connection to Other Concepts

- [[first-passage-time]] supplies return-time distributions.
- [[stationary-distribution]] exists for positive recurrent irreducible chains.
- [[basic-limit-theorem]] turns recurrence into limiting probabilities.

## Theorems

- [[basic-limit-theorem]]
- [[finite-state-positive-recurrence]]
- [[transience-criterion]]

## Examples

- M/G/1 embedded chain: positive recurrent if $\rho<1$, null recurrent if $\rho=1$, transient if $\rho>1$.

## Open Questions / Gaps

> [!todo] Gap - Add worked page specifically for M/G/1 recurrence classification.

## Sources

- [[sources/lecture-notes-ch3]] - recurrence, state categories, finite-state facts.

