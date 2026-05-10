---
type: concept
tags: [stochastic-processes, markov-chains, discrete-time]
sources: [lecture-notes-ch2]
related: [markov-chain, chapman-kolmogorov, stationary-distribution]
---

# Transition Matrix

**A transition matrix is the row-stochastic matrix of one-step transition probabilities for a homogeneous Markov chain.**

## Definition

For a homogeneous Markov chain,
$$
P_{ij}=\mathbb{P}[X_{n+1}=j\mid X_n=i],
$$
with $P_{ij}\geq 0$ and $\sum_jP_{ij}=1$ for every state $i$.

## Key Properties

- Rows are probability distributions.
- $\mathbf{P}^n$ gives $n$-step transition probabilities.
- Stationary distributions solve $\pi=\pi P$.
- Absorbing chains decompose $\mathbf{P}$ into blocks $\mathbf{Q}$ and $\mathbf{R}$.

## Intuition

Each row says where the process can go next from the current state.

## Connection to Other Concepts

- [[markov-chain]] uses transition matrices as its finite description.
- [[stationary-distribution]] is an invariant row vector for the matrix.
- [[fundamental-matrix]] is built from the transient block.

## Theorems

- [[chapman-kolmogorov]]
- [[fundamental-matrix]]

## Examples

- Two-state chain $\begin{pmatrix}1-a&a\\b&1-b\end{pmatrix}$.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch2]] - definition and matrix powers.

