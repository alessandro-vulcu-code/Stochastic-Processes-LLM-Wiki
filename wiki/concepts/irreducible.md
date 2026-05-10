---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[concepts/communicating-classes]], [[concepts/state-classification]], [[concepts/positive-recurrent]]
---

# Irreducible

**A Markov chain is irreducible when all states communicate with one another.**

## Definition

States $i$ and $j$ communicate, written $i\leftrightarrow j$, when each is reachable from the other:
$$
\exists n,m\geq 0:\quad P_{ij}^{(n)}>0,\qquad P_{ji}^{(m)}>0.
$$
A chain is irreducible if it has a single communicating class.

## Key Properties

- Recurrence, transience, period, positive recurrence, and null recurrence are class properties.
- In an irreducible chain, proving a classification for one state proves it for all states.
- Irreducibility plus aperiodicity and positive recurrence gives convergence to a unique limiting distribution.

## Intuition

Irreducibility means the chain is one connected probabilistic component rather than several isolated regions.

## Connection to Other Concepts

This refines [[concepts/communicating-classes|Communicating Classes]] and is used by [[theorems/basic-limit-theorem|Basic Limit Theorem]].

## Theorems

- [[theorems/basic-limit-theorem|Basic Limit Theorem]]
- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]

## Examples

- A random walk on $\mathbb{Z}$ with positive probabilities of stepping left and right is irreducible.

## Open Questions / Gaps

> [!todo] Gap - Add graphical algorithms for finding communicating classes.

## Sources

- [[sources/lecture-notes-ch3]] - class structure and long-run classification.
