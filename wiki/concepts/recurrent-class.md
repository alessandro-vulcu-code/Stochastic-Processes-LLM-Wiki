---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[communicating-classes]], [[recurrence]], [[positive-recurrent]], [[null-recurrent]], [[stationary-distribution]]
---

# Recurrent Class / Transient Class

**A recurrent class is a communicating class in which every state is recurrent; a transient class contains only transient states.**

## Definition

A **recurrent class** $C$ is a communicating class such that:
- Every state $i \in C$ is recurrent ($f_{ii} = 1$).
- The class is **closed** (isolated): $P_{ij}^{(n)} = 0$ for all $i \in C$, $j \notin C$, and all $n \geq 0$.

A **transient class** is a communicating class whose states are all transient.

## Key Properties

- A recurrent class is necessarily closed: once entered, it cannot be left.
- The submatrix $\|P_{ij}\|$ with $i,j \in C$ is itself a transition matrix of an irreducible Markov chain.
- **Positive recurrent class:** finite mean return time $m_i < \infty$ for all $i \in C$; limiting probabilities $\pi_i > 0$.
- **Null recurrent class:** $m_i = \infty$ for all $i \in C$; limiting probabilities $\pi_i = 0$.
- Finite Markov chains have no null recurrent states — every recurrent class is positive recurrent.

## Intuition

Recurrent classes act as absorbing islands: the chain wanders among transient states until it falls into one and never leaves. Within a positive recurrent class, the basic limit theorem applies directly.

## Connection to Other Concepts

- [[communicating-classes]] — classes as building blocks.
- [[positive-recurrent]], [[null-recurrent]] — classify recurrent classes further.
- [[stationary-distribution]] — exists uniquely for each positive recurrent class.
- [[absorbing-markov-chain]] — special case where recurrent classes are single absorbing states.
- [[basic-limit-theorem]] — applies inside aperiodic recurrent classes.

## Theorems

- [[basic-limit-theorem]]
- [[stationary-distribution-positive-recurrent-class]]
- [[finite-state-positive-recurrence]]

## Sources

- [[sources/lecture-notes-ch3]] — §3.4, §3.6, Table 3.1, Table 3.2.
