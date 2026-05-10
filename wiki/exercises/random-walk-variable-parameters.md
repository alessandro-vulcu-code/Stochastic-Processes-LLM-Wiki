---
type: exercise
tags: [exercise, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [random-walk, transience-criterion, recurrence]
---

# Random Walk with Variable Parameters

## Problem

Classify a random walk on $\mathbb{N}$ with reflecting boundary at 0 and transition probabilities $P_{i,i+1}=p_i$, $P_{i,i-1}=q_i=1-p_i$.

## Solution

Apply the transience criterion by solving
$$
Z_i=p_iZ_{i+1}+q_iZ_{i-1}.
$$
Differences satisfy
$$
Z_{i+1}-Z_i=\frac{q_i}{p_i}(Z_i-Z_{i-1}),
$$
so
$$
Z_{n+1}-Z_0=Z_1\sum_{i=0}^n\prod_{j=1}^i\frac{q_j}{p_j}.
$$
A bounded nonzero solution exists iff
$$
\sum_{i=0}^{\infty}\prod_{j=1}^i\frac{q_j}{p_j}<\infty,
$$
which gives transience. The source also records the complementary positive-recurrence condition through products of $p_j/q_j$ and identifies the remaining divergent case as null recurrence.

## Concepts

- [[concepts/random-walk]]
- [[theorems/transience-criterion]]
- [[concepts/recurrence]]

## Sources

- [[sources/lecture-notes-ch3]]

