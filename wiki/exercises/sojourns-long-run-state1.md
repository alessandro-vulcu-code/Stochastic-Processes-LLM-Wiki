---
type: exercise
tags: [exercise, renewal-process, markov-chains]
sources: [lecture-notes-ch5]
related: [alternating-renewal-process, regenerative-process]
---

# Sojourns and Long-Run Fraction in State 1

## Problem

For the Markov chain with transition matrix
$$
P=\begin{pmatrix}
0.3&0.7&0\\
0.6&0&0.4\\
0&0.5&0.5
\end{pmatrix},
$$
find the mean duration of a sojourn in state $0$ and the long-run fraction of time in state $1$ using renewal theory.

## Solution

A sojourn in state $0$ ends with probability $0.7$ at each step, so its mean duration is
$$
\mathbb{E}[\text{stay in }0]=\frac{1}{0.7}=\frac{10}{7}.
$$

Visits to state $1$ are regenerative. The chain spends exactly one time unit in state $1$, so $\mathbb{E}[Y]=1$. Starting from state $1$, after one step it goes to state $0$ with probability $0.6$ and to state $2$ with probability $0.4$. The mean stay in state $2$ is $1/0.5=2$. Hence the mean cycle length is
$$
\mathbb{E}[X]=1+0.6\cdot\frac{10}{7}+0.4\cdot2=\frac{93}{35}.
$$
The long-run fraction in state $1$ is
$$
\boxed{\frac{\mathbb{E}[Y]}{\mathbb{E}[X]}=\frac{35}{93}}.
$$

## Concepts

- [[concepts/alternating-renewal-process|Alternating Renewal Process]]
- [[concepts/regenerative-process|Regenerative Process]]
- [[theorems/renewal-reward-theorem|Renewal Reward Theorem]]

## Sources

- [[sources/lecture-notes-ch5]]
