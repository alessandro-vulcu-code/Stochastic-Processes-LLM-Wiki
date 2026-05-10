---
type: exercise
tags: [exercise, markov-chains, random-walk]
sources: [lecture-notes-ch2]
related: [random-walk, first-step-analysis]
---

# Gambler's Ruin

## Problem

A random walk on $\{0,1,\ldots,N\}$ has absorbing states 0 and $N$. From $k$ it moves to $k+1$ with probability $p$ and to $k-1$ with probability $q=1-p$. Find the probability $u_k$ of absorption at 0 starting from $k$.

## Solution

First-step analysis gives
$$
u_k=pu_{k+1}+qu_{k-1},\qquad u_0=1,\quad u_N=0.
$$
Let $x_k=u_k-u_{k-1}$. Then
$$
x_{k+1}=\frac{q}{p}x_k.
$$
Solving and applying the boundary conditions:
$$
u_k=
\begin{cases}
\dfrac{N-k}{N}, & p=q=1/2,\\[6pt]
\dfrac{(q/p)^k-(q/p)^N}{1-(q/p)^N}, & p\neq q.
\end{cases}
$$

For $N\to\infty$, $u_k=1$ if $p\leq q$ and $u_k=(q/p)^k$ if $p>q$.

## Concepts

- [[concepts/random-walk]]
- [[concepts/first-step-analysis]]
- [[concepts/absorbing-markov-chain]]

## Sources

- [[sources/lecture-notes-ch2]]

