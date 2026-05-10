---
type: exercise
tags: [exercise, markov-chains, absorption]
sources: [lecture-notes-ch3]
related: [absorbing-markov-chain, first-step-analysis]
---

# Last Toss Coins Absorption

## Problem

Five fair coins are tossed. Coins showing tails are tossed again until all coins show heads. Let $X$ be the number of coins involved in the last toss. Find $\mathbb{P}[X=1]$.

## Solution

Let the state be the number of coins still showing tails. The state can decrease or stay the same. Make states 0 and 1 absorbing: absorption in 1 means the last toss involves exactly one coin; absorption in 0 means the process skipped directly to all heads.

Let $u_i$ be the probability of absorption in 1 from state $i$. Boundary values are $u_0=0$, $u_1=1$. For $i\geq2$, first-step analysis uses Binomial transition probabilities:
$$
u_i=\sum_{j=0}^i \binom{i}{j}2^{-i}u_j.
$$
Solving the finite linear system for $i=2,\ldots,5$ gives
$$
u_5\approx 0.7235.
$$

## Concepts

- [[concepts/absorbing-markov-chain]]
- [[concepts/first-step-analysis]]

## Sources

- [[sources/lecture-notes-ch3]]

