---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [fundamental-matrix, absorbing-markov-chain]
---

# Mean Absorption Time via Fundamental Matrix

**Mean absorption times are row sums of the fundamental matrix.**

## Statement (Formal)

For transient states,
$$
\boldsymbol{\nu}=\mathbf{W}\mathbf{1}=(I-\mathbf{Q})^{-1}\mathbf{1}.
$$

## Proof Sketch

Sum $W_{ij}$ over all transient states $j$. At each pre-absorption time exactly one transient-state indicator is one, so the total expected count equals expected absorption time.

## Conditions

The chain must be in absorbing canonical form with transient block $\mathbf{Q}$.

## Consequences

Avoids solving one first-step system by hand for each starting state.

## Related Theorems

- [[fundamental-matrix]]

## Sources

- [[sources/lecture-notes-ch2]]

