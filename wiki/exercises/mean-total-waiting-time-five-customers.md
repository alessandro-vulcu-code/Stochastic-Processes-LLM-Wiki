---
type: exercise
tags: [exercise, poisson-process, conditional-arrivals]
sources: [lecture-notes-ch4]
related: [conditional-arrival-times-uniform]
---

# Mean Total Arrival Time for Five Customers

## Problem

Customers arrive according to a Poisson process. Given that five customers arrived in the first hour, find
$$
\mathbb{E}[W_1+W_2+W_3+W_4+W_5].
$$

## Solution

Given five arrivals in $[0,1]$, the unordered arrival times are i.i.d. uniform on $[0,1]$. The sum is unaffected by ordering, so each has mean $1/2$.

Hence
$$
\boxed{\mathbb{E}[W_1+\cdots+W_5]=5\cdot\frac12=\frac52\text{ hours}}.
$$

## Concepts

- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]]
- [[concepts/uniform-distribution|Uniform Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
