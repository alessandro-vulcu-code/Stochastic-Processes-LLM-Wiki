---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch3]
related: [[communicating-classes]], [[markov-chain]], [[recurrence]]
---

# Accessible State

**State $j$ is accessible from state $i$ if it can be reached from $i$ in some finite number of steps.**

## Definition

State $j$ is **accessible** from state $i$, written $i \to j$, if:
$$P_{ij}^{(n)} > 0 \quad \text{for some } n \geq 0$$

If $i \to j$ and $j \to i$, the states **communicate**: $i \leftrightarrow j$.

Communication is an equivalence relation and partitions the state space into **communicating classes**.

## Key Properties

- Every state is accessible from itself ($n = 0$, since $P_{ii}^{(0)} = 1$).
- Transitivity: if $i \to j$ and $j \to k$, then $i \to k$.
- Non-communicating states: $P_{ij}^{(n)} = 0$ or $P_{ji}^{(n)} = 0$ for all $n \geq 0$.

## Intuition

Accessibility formalizes whether one state can "see" another. A chain is irreducible exactly when every state is accessible from every other — one big communicating class.

## Connection to Other Concepts

- [[communicating-classes]] — defined by mutual accessibility.
- [[irreducible]] — all states mutually accessible.
- [[recurrence]] — recurrence is a class property, so accessible states share it.

## Sources

- [[sources/lecture-notes-ch3]] — definition at §3.1, summary table §3.9.
