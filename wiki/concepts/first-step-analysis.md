---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [markov-chain, conditional-probability, absorbing-markov-chain]
---

# First-Step Analysis

**First-step analysis conditions on the first transition of a Markov chain to derive recursive linear equations.**

## Definition

For an unknown quantity $u_i$ starting from state $i$, condition on $X_1$:
$$
u_i=\sum_j P_{ij}u_j
$$
with boundary terms added when the first step immediately resolves the target event.

## Key Properties

- Converts hitting probabilities into linear equations.
- Converts mean hitting/absorption times into linear equations with a $+1$ term.
- Boundary conditions come from absorbing or target states.

## Intuition

Take one step, pay the immediate cost or probability contribution, then restart the same problem from the new state.

## Connection to Other Concepts

- [[conditional-probability]] is the underlying operation.
- [[absorbing-markov-chain]] uses first-step equations for absorption probabilities and times.
- [[fundamental-matrix]] gives a matrix form of the same computations.

## Theorems

- [[mean-first-passage-time]]
- [[mean-absorption-time]]
- [[absorption-probabilities]]

## Examples

- [[gambler-ruin]]
- [[urn-removal-mean-duration]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch2]] - first-step examples and matrix form.
- [[sources/lecture-notes-ch3]] - absorption and transience exercises.

