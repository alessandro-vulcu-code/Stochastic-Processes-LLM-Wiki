---
type: exercise
tags: [exercise, markov-chains, absorption]
sources: [lecture-notes-ch3]
related: [first-step-analysis, absorbing-markov-chain]
---

# Urn Removal Mean Duration

## Problem

An urn contains five red and three green balls. Red balls are removed when drawn; green balls are returned. Drawing continues until all red balls are removed. Find the mean game duration.

## Solution

Let $X_n$ be the number of red balls remaining. From state $i$, the probability of staying at $i$ is the probability of drawing green:
$$
a_i=\frac{3}{i+3},
$$
and the probability of moving to $i-1$ is $1-a_i=i/(i+3)$.

The mean absorption time satisfies
$$
\nu_i=1+a_i\nu_i+(1-a_i)\nu_{i-1},
$$
so
$$
\nu_i=\frac{1}{1-a_i}+\nu_{i-1}.
$$
Thus
$$
\nu_5=\frac85+\frac74+2+\frac52+4=11.85.
$$

## Concepts

- [[concepts/first-step-analysis]]
- [[concepts/absorbing-markov-chain]]

## Sources

- [[sources/lecture-notes-ch3]]

