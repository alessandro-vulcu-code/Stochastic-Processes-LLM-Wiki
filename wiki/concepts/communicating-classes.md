---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch3]
related: [markov-chain, recurrence, period]
---

# Communicating Classes

**Communicating classes are equivalence classes of states under mutual accessibility.**

## Definition

State $j$ is accessible from $i$ if $P_{ij}^{(n)}>0$ for some $n\geq 0$. States $i$ and $j$ communicate, written $i\leftrightarrow j$, if each is accessible from the other.

The relation $\leftrightarrow$ is reflexive, symmetric, and transitive, so it partitions the state space into classes.

## Key Properties

- A chain with one communicating class is irreducible.
- Distinct classes can be connected only one way.
- Period, recurrence, and positive/null recurrence are class properties.
- Recurrent classes are closed.

## Intuition

Communication means two states belong to the same navigable region of the chain.

## Connection to Other Concepts

- [[period]] is constant on a class.
- [[recurrence]] is a class property.
- [[stationary-distribution]] is often computed class by class.

## Theorems

- [[period-class-property]]
- [[basic-limit-theorem]]
- [[transient-to-recurrent-limit]]

## Examples

- Reducible chains with closed recurrent classes and transient states feeding into them.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch3]] - accessibility, communication, irreducibility.

