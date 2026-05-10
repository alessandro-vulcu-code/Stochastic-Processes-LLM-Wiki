---
type: exercise
tags: [exercise, markov-chains, queueing, recurrence]
sources: [lecture-notes-ch3]
related: [g-m-1-queue, positive-recurrent]
---

# G/M/1 Positive Recurrence

## Problem

Determine when the embedded G/M/1 queue is positive recurrent from its transition probabilities.

## Solution

The chain is irreducible and aperiodic, so a normalized stationary solution is enough. Use the ansatz
$$
\pi_k=c\beta^k,\qquad 0<\beta<1.
$$
Substitution into the stationarity equations gives the fixed-point equation
$$
\beta=A(\beta)=\int_0^\infty e^{-\mu t(1-\beta)}\,dG(t).
$$

Since $A(1)=1$ and
$$
A'(1)=\mu\mathbb{E}[T]=\frac{\mu}{\lambda},
$$
a nontrivial solution $\beta^*\in(0,1)$ exists in the stable case $\lambda<\mu$. Then $\pi_k=c(\beta^*)^k$ is normalizable and the chain is positive recurrent.

The classification recorded in the source is:

- $\lambda<\mu$: positive recurrent.
- $\lambda=\mu$: null recurrent.
- $\lambda>\mu$: transient.

## Concepts

- [[concepts/g-m-1-queue|G/M/1 Queue]]
- [[concepts/positive-recurrent|Positive Recurrent]]
- [[concepts/stationary-distribution|Stationary Distribution]]

## Sources

- [[sources/lecture-notes-ch3]]
