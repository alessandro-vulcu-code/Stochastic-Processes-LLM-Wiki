---
type: exercise
tags: [exercise, poisson-process, exponential-distribution]
sources: [lecture-notes-ch4]
related: [poisson-process, exponential-distribution]
---

# First Time All Processes Fire

## Problem

For $i=1,\ldots,n$, let $X_i(t)$ be independent Poisson processes with common rate $\lambda$. Find the distribution of the first time $T$ at which every process has had at least one event.

## Solution

Let $T_i$ be the first arrival time of process $i$. Then $T_i\sim\mathrm{Exp}(\lambda)$ independently, and
$$
T=\max(T_1,\ldots,T_n).
$$
Therefore
$$
\mathbb{P}(T\leq t)=\prod_{i=1}^n\mathbb{P}(T_i\leq t)
=\boxed{(1-e^{-\lambda t})^n}.
$$

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[concepts/exponential-distribution|Exponential Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
