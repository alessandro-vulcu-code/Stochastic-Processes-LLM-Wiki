---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [first-step-analysis, fundamental-matrix]
---

# Absorbing Markov Chain

**An absorbing Markov chain has states that, once entered, cannot be left.**

## Definition

A state $i$ is absorbing if $P_{ii}=1$. After reordering states so transient states come first and absorbing states last,
$$
\mathbf{P}=\begin{pmatrix}\mathbf{Q}&\mathbf{R}\\0&I\end{pmatrix}.
$$

## Key Properties

- Transient block $\mathbf{Q}$ governs motion before absorption.
- Absorption probabilities solve first-step equations.
- Expected time before absorption is the row sum of the fundamental matrix.

## Intuition

The chain wanders among transient states until it falls into a terminal class.

## Connection to Other Concepts

- [[fundamental-matrix]] gives expected visits before absorption.
- [[first-step-analysis]] computes absorption probabilities and times.
- Reducible long-run chains often reduce to absorption into recurrent classes.

## Theorems

- [[fundamental-matrix]]
- [[mean-absorption-time]]
- [[absorption-probabilities]]
- [[transient-to-recurrent-limit]]

## Examples

- [[gambler-ruin]]
- [[last-toss-coins-absorption]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch2]] - absorbing-chain block form and formulas.
- [[sources/lecture-notes-ch3]] - absorption into recurrent classes.

