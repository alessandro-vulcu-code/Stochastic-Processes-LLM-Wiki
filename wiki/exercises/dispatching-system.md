---
type: exercise
tags: [exercise, poisson-process, cost]
sources: [lecture-notes-ch4]
related: [poisson-process, expected-value]
---

# Dispatching System

## Problem

Customers arrive according to a Poisson process of rate $\lambda$. They are dispatched at fixed times $T,2T,\ldots$. Waiting costs $c$ per customer per unit time and each dispatch costs $K$. Find the average cost per unit time and the optimal $T$.

## Solution

The dispatch cost per cycle is $K$. The expected waiting cost in one cycle is
$$
c\int_0^T\mathbb{E}[X(t)]\,dt
=c\int_0^T\lambda t\,dt
=\frac{c\lambda T^2}{2}.
$$

Average cost per unit time:
$$
C(T)=\frac{K+c\lambda T^2/2}{T}.
$$
Minimize:
$$
C'(T)=-\frac{K}{T^2}+\frac{c\lambda}{2}=0
\quad\Rightarrow\quad
\boxed{T^*=\sqrt{\frac{2K}{c\lambda}}}.
$$

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[concepts/expected-value|Expected Value]]

## Sources

- [[sources/lecture-notes-ch4]]
