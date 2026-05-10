---
type: exercise
tags: [exercise, markov-chains, absorbing-chain]
sources: [lecture-notes-ch2]
related: [absorbing-markov-chain, first-step-analysis]
---

# Four-State Absorbing Chain

## Problem

A chain has absorbing states $0$ and $3$ and transient states $1$ and $2$. Write first-step equations for the probability of absorption in $0$ and for the mean absorption time.

## Solution

Let
$$
u_i=\mathbb{P}(X_T=0\mid X_0=i),\qquad i=1,2.
$$
With $u_0=1$ and $u_3=0$, first-step analysis gives
$$
u_1=P_{10}+P_{11}u_1+P_{12}u_2,
$$
$$
u_2=P_{20}+P_{21}u_1+P_{22}u_2.
$$

For mean absorption times $\nu_i=\mathbb{E}[T\mid X_0=i]$, absorbing states contribute zero remaining time:
$$
\nu_1=1+P_{11}\nu_1+P_{12}\nu_2,
$$
$$
\nu_2=1+P_{21}\nu_1+P_{22}\nu_2.
$$

## Concepts

- [[concepts/absorbing-markov-chain|Absorbing Markov Chain]]
- [[concepts/first-step-analysis|First-Step Analysis]]
- [[concepts/fundamental-matrix|Fundamental Matrix]]

## Sources

- [[sources/lecture-notes-ch2]]
