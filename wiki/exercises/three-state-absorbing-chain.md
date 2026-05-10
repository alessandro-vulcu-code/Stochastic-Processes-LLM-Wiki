---
type: exercise
tags: [exercise, markov-chains, absorbing-chain]
sources: [lecture-notes-ch2]
related: [absorbing-markov-chain, first-step-analysis]
---

# Three-State Absorbing Chain

## Problem

Consider a chain with absorbing states $0$ and $2$, and transient state $1$:
$$
P=\begin{array}{c|ccc}
&0&1&2\\ \hline
0&1&0&0\\
1&\alpha&\beta&\gamma\\
2&0&0&1
\end{array}.
$$
Starting from state $1$, find the probability of absorption in $0$ and the mean absorption time.

## Solution

Let
$$
u=\mathbb{P}(X_T=0\mid X_0=1).
$$
First-step analysis gives
$$
u=\alpha+\beta u,
$$
so
$$
\boxed{u=\frac{\alpha}{1-\beta}=\frac{\alpha}{\alpha+\gamma}}.
$$

Let $\nu=\mathbb{E}[T\mid X_0=1]$. Counting the first step:
$$
\nu=1+\beta\nu,
$$
so
$$
\boxed{\nu=\frac{1}{1-\beta}}.
$$

## Concepts

- [[concepts/absorbing-markov-chain|Absorbing Markov Chain]]
- [[concepts/first-step-analysis|First-Step Analysis]]
- [[theorems/mean-absorption-time|Mean Absorption Time via Fundamental Matrix]]

## Sources

- [[sources/lecture-notes-ch2]]
