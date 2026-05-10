---
type: exercise
tags: [exercise, markov-chains, periodicity]
sources: [lecture-notes-ch4]
related: [period, limiting-probability-distribution]
---

# Periodic Class and Existence of the General Limit

## Problem

A reducible transition matrix has a transient block $Q$, an absorbing block, and a recurrent class
$$
A=\begin{pmatrix}0&1\\1&0\end{pmatrix}
$$
of period $2$. The transient block can enter the periodic class through $R_1$. Determine when the full limit of $P^n$ exists.

## Solution

The problematic block in $P^{n+1}$ is
$$
\sum_{i=0}^{n}Q^iR_1A^{n-i}.
$$
Even and odd $n$ give different limits unless
$$
R_1=R_1A.
$$
Since multiplying by $A$ swaps the two columns of $R_1$, the general limit exists iff the two columns of $R_1$ are identical.

## Concepts

- [[concepts/period|Period]]
- [[concepts/aperiodic|Aperiodic]]
- [[concepts/limiting-probability-distribution|Limiting Probability Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
