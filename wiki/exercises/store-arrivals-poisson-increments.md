---
type: exercise
tags: [exercise, poisson-process, independent-increments]
sources: [lecture-notes-ch4]
related: [poisson-process]
---

# Store Arrivals via Independent Increments

## Problem

Customers arrive at rate $\lambda=4$ per hour. Starting at 9:00, find the probability that exactly one customer has arrived by 9:30 and exactly five have arrived by 11:30.

## Solution

Use hours as units. The event is $\{X(1/2)=1,\ X(5/2)=5\}$, equivalently one arrival in $(0,1/2]$ and four arrivals in $(1/2,5/2]$.

By independent increments:
$$
\mathbb{P}(X(1/2)=1)\mathbb{P}(X(5/2)-X(1/2)=4)
=2e^{-2}\cdot \frac{8^4e^{-8}}{4!}.
$$
Thus
$$
\mathbb{P}=\frac{1024}{3}e^{-10}\approx 0.0155.
$$

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[concepts/poisson-distribution|Poisson Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
