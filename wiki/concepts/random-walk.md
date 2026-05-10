---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [markov-chain, recurrence, first-step-analysis]
---

# Random Walk

**A random walk is a Markov chain whose state changes by local steps, usually to neighbouring states.**

## Definition

On $\mathbb{N}$ or a finite line, a one-dimensional random walk can have
$$
P_{i,i+1}=p_i,\qquad P_{i,i-1}=q_i,\qquad P_{ii}=r_i,
$$
with $p_i+q_i+r_i=1$.

## Key Properties

- Absorbing boundaries model ruin or termination.
- Recurrence/transience depends on drift and, in variable walks, products of local odds ratios.
- First-step analysis solves hitting probabilities.

## Intuition

The process is a particle or resource level that moves locally, one step at a time.

## Connection to Other Concepts

- [[gambler-ruin]] is the canonical finite absorbing random walk.
- [[recurrence]] classifies infinite random walks.
- [[transience-criterion]] gives a bounded-solution test.

## Theorems

- [[transience-criterion]]

## Examples

- [[gambler-ruin]]
- [[random-walk-variable-parameters]]

## Open Questions / Gaps

> [!todo] Gap - Add a clean comparison between biased, unbiased, finite, and reflected random walks.

## Sources

- [[sources/lecture-notes-ch2]] - random-walk and gambler's ruin examples.
- [[sources/lecture-notes-ch3]] - variable-parameter classification.

