---
type: exercise
tags: [exercise, markov-chains, queueing, recurrence]
sources: [lecture-notes-ch3]
related: [m-g-1-queue, probability-generating-function, state-classification]
---

# M/G/1 Classification

## Problem

Classify the embedded M/G/1 departure chain in terms of
$$
\rho=\sum_{n=0}^{\infty}n a_n,
$$
the mean number of arrivals during one service time.

## Solution

Solving the stationary equations with probability generating functions gives
$$
\pi(s)=\pi_0\frac{(s-1)A(s)}{s-A(s)},
$$
where $A(s)=\sum_{n\geq0}a_ns^n$. Normalization at $s=1$ gives
$$
\pi_0=1-\rho.
$$
Thus a normalized stationary distribution exists when $\rho<1$, proving positive recurrence.

For transience, the source uses the bounded-harmonic criterion with ansatz $Z_i=1-s^i$, leading to $s=A(s)$. A nonzero bounded solution exists when $\rho>1$, so the chain is transient.

At $\rho=1$, a divergent solution to the recurrence inequality exists, proving recurrence; since it is not positive recurrent, it is null recurrent.

Therefore:

- $\rho<1$: positive recurrent.
- $\rho=1$: null recurrent.
- $\rho>1$: transient.

## Concepts

- [[concepts/m-g-1-queue|M/G/1 Queue]]
- [[concepts/probability-generating-function|Probability Generating Function]]
- [[concepts/state-classification|State Classification]]

## Sources

- [[sources/lecture-notes-ch3]]
