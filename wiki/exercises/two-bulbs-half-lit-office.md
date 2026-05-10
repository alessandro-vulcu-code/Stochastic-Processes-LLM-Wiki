---
type: exercise
tags: [exercise, renewal-process, reliability]
sources: [lecture-notes-ch5]
related: [renewal-reward-process, excess-life]
---

# Two Bulbs and Half-Lit Office

## Problem

Two bulbs start working. When one fails, replacement is delayed until the second fails, then both are replaced immediately. Find the long-run fraction of time the office is half lit.

## Solution

Each replacement-to-replacement interval is a renewal cycle. The half-lit time is the time between the first and second bulb failures.

For equal exponential lifetimes with rate $\beta$, the first failure time is exponential with rate $2\beta$, so its mean is $1/(2\beta)$. After the first failure, memorylessness gives mean remaining time $1/\beta$. Thus the fraction half lit is
$$
\frac{1/\beta}{1/(2\beta)+1/\beta}=\frac23.
$$

For non-exponential lifetimes, memorylessness cannot be used; one must compute expected order-statistic gaps from the lifetime distribution. The source treats uniform $(0,1)$ as the second case using this renewal-cycle method.

## Concepts

- [[concepts/renewal-reward-process]]
- [[concepts/excess-life]]
- [[concepts/exponential-distribution]]

## Sources

- [[sources/lecture-notes-ch5]]

