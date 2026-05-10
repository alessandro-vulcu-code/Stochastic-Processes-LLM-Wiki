---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[recurrence]], [[lemma-maximal-bounded-solution]], [[lemma-recurrence-criterion-state-0]]
---

# Lemma 3.7.1 — Monotonicity of Survival Probabilities

**The $n$-step survival probability $Y_i(n)$ is non-increasing in $n$ for every state $i$.**

## Statement (Formal)

Let $S \subseteq \mathbb{N}$ and define $Y_i(n) = \mathbb{P}[\text{chain stays in } S \text{ for } n \text{ steps} \mid X_0 = i]$. Then:

$$Y_i(n) \geq Y_i(n+1) \qquad \forall i \in S,\; n \geq 1$$

where $Y_i(n)$ satisfies the recursion:
$$Y_i(n) = \sum_{j \in S} P_{ij}\,Y_j(n-1), \qquad Y_i(1) = \sum_{j \in S} P_{ij}$$

## Proof Sketch

By induction. Base case $n=2$:
$$Y_i(2) = \sum_{j \in S} P_{ij} Y_j(1) \leq \sum_{j \in S} P_{ij} = Y_i(1)$$
since $Y_j(1) \leq 1$. Inductive step uses the same substitution. $\blacksquare$

Consequence: $Y_i(n)$ is bounded in $[0,1]$ and non-increasing, so $Y_i = \lim_{n\to\infty} Y_i(n)$ exists and satisfies:
$$Y_i = \sum_{j \in S} P_{ij} Y_j$$

## Conditions

- State space $S$ is any subset of $\mathbb{N}$.
- No irreducibility required.

## Consequences

- Guarantees that the limiting survival probability $Y_i$ is well-defined.
- $Y_i$ = probability chain starting at $i$ never leaves $S$.
- Enables [[lemma-maximal-bounded-solution]]: $Y_i$ is the maximal bounded solution.

## Related Theorems

- [[lemma-maximal-bounded-solution]] — $Y_i$ dominates all bounded solutions.
- [[lemma-recurrence-criterion-state-0]] — uses $Y_i$ to characterize recurrence.
- [[recurrence-criterion]] — $\sum_n P_{ii}^{(n)} = \infty \iff i$ recurrent.

## Sources

- [[sources/lecture-notes-ch3]] — §3.7, Lemma 3.7.1.
