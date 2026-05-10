---
type: exercise
tags: [exercise, markov-chains, stationary-distribution]
sources: [lecture-notes-ch4]
related: [stationary-distribution]
---

# Backward Probability

## Problem

After a long time, a regular Markov chain is observed in state $1$. Find
$$
\lim_{n\to\infty}\mathbb{P}(X_{n-1}=2\mid X_n=1).
$$

## Solution

Use conditional probability:
$$
\mathbb{P}(X_{n-1}=2\mid X_n=1)
=P_{21}\frac{\mathbb{P}(X_{n-1}=2)}{\mathbb{P}(X_n=1)}.
$$
Taking the limit:
$$
\boxed{\lim_{n\to\infty}\mathbb{P}(X_{n-1}=2\mid X_n=1)
=P_{21}\frac{\pi_2}{\pi_1}}.
$$

For the specific matrix in the source, this equals $6/35$.

## Concepts

- [[concepts/stationary-distribution|Stationary Distribution]]
- [[concepts/conditional-probability|Conditional Probability]]

## Sources

- [[sources/lecture-notes-ch4]]
