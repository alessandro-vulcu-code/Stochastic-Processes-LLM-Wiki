---
type: exercise
tags: [exercise, poisson-approximation]
sources: [lecture-notes-ch4]
related: [poisson-limit-theorem]
---

# Typographical Errors

## Problem

A 600-page book contains 240 typographical errors uniformly distributed. Use a Poisson approximation to find the probability that three particular successive pages are error-free.

## Solution

For one page, the approximate mean number of errors is
$$
240\cdot\frac{1}{600}=0.4.
$$
For three pages, the mean is $1.2$. Thus
$$
\boxed{\mathbb{P}(\text{three pages error-free})\approx e^{-1.2}}.
$$

## Concepts

- [[concepts/poisson-distribution|Poisson Distribution]]
- [[theorems/poisson-limit-theorem|Poisson Limit Theorem]]

## Sources

- [[sources/lecture-notes-ch4]]
