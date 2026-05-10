---
type: exercise
tags: [exercise, markov-chains, protocols]
sources: [lecture-notes-ch2]
related: [first-step-analysis, absorbing-markov-chain]
---

# Layer 2 Protocol Throughput

## Problem

A packet is transmitted up to $L+1$ times. Each attempt fails with probability $\epsilon$ and succeeds with probability $1-\epsilon$. Find the success probability, mean number of attempts, and throughput.

## Solution

Let $u_i$ be the probability of eventual success after $i$ failures. For $i<L$,
$$
u_i=\epsilon u_{i+1}+1-\epsilon,\qquad u_L=1-\epsilon.
$$
Backward recursion gives
$$
u_0=1-\epsilon^{L+1}.
$$

Let $\nu_i$ be the mean number of attempts. Then
$$
\nu_i=1+\epsilon\nu_{i+1},\qquad \nu_L=1,
$$
so
$$
\nu_0=\frac{1-\epsilon^{L+1}}{1-\epsilon}.
$$
Throughput is success probability divided by mean attempts:
$$
\frac{u_0}{\nu_0}=1-\epsilon.
$$

## Concepts

- [[concepts/first-step-analysis]]
- [[concepts/absorbing-markov-chain]]

## Sources

- [[sources/lecture-notes-ch2]]

