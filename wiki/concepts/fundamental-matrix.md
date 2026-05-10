---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch2]
related: [absorbing-markov-chain, first-step-analysis]
---

# Fundamental Matrix

**The fundamental matrix $\mathbf{W}=(I-\mathbf{Q})^{-1}$ gives expected transient-state visits before absorption.**

## Definition

For an absorbing Markov chain with transient block $\mathbf{Q}$,
$$
\mathbf{W}=I+\mathbf{Q}+\mathbf{Q}^2+\cdots=(I-\mathbf{Q})^{-1}.
$$
The entry $W_{ij}$ is the expected number of visits to transient state $j$ before absorption, starting from transient state $i$.

## Key Properties

- Row sums give mean absorption times.
- Multiplication by $\mathbf{R}$ gives absorption probabilities.
- It is the matrix analogue of the geometric sum $(1-q)^{-1}$.

## Intuition

Each power $\mathbf{Q}^n$ counts visits after $n$ transient steps. Summing all powers counts all expected visits before the process exits the transient set.

## Connection to Other Concepts

- [[absorbing-markov-chain]] supplies $\mathbf{Q}$ and $\mathbf{R}$.
- [[first-step-analysis]] gives equivalent linear equations.

## Theorems

- [[fundamental-matrix]]
- [[mean-absorption-time]]
- [[absorption-probabilities]]

## Examples

- Finite absorbing chains with multiple transient states.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch2]] - definition, derivation, and applications.

