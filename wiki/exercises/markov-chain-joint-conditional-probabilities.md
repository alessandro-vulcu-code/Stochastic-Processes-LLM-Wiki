---
type: exercise
tags: [exercise, markov-chains, conditional-probability]
sources: [lecture-notes-ch2]
related: [markov-chain-factorization, n-step-transition-probability]
---

# Markov Chain Joint and Conditional Probabilities

## Problem

A Markov chain on states $0,1,2$ has transition matrix
$$
P=\begin{pmatrix}
0.1&0.2&0.7\\
0.9&0.1&0\\
0.1&0.8&0.1
\end{pmatrix}
$$
and initial distribution $p=(0.3,0.4,0.3)^T$. Compute path and conditional probabilities such as $\mathbb{P}(X_0=0,X_1=1,X_2=1)$ and $\mathbb{P}(X_3=1,X_1=1\mid X_0=0)$.

## Solution

Use Markov-chain path factorization:
$$
\mathbb{P}(X_0=i_0,\ldots,X_n=i_n)
=p_{i_0}P_{i_0i_1}\cdots P_{i_{n-1}i_n}.
$$
Thus
$$
\mathbb{P}(X_0=0,X_1=1,X_2=1)
=0.3\cdot0.2\cdot0.1=0.006.
$$

For nonconsecutive times, use an $n$-step probability:
$$
\mathbb{P}(X_3=1,X_1=1\mid X_0=0)=P_{01}P_{11}^{(2)}.
$$

## Concepts

- [[concepts/markov-chain|Markov Chain]]
- [[concepts/initial-distribution|Initial Distribution]]
- [[concepts/n-step-transition-probability|n-Step Transition Probability]]
- [[theorems/markov-chain-factorization|Markov Chain Factorization]]

## Sources

- [[sources/lecture-notes-ch2]]
