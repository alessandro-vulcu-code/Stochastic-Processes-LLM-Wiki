---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[concepts/period]], [[concepts/irreducible]], [[concepts/limiting-probability-distribution]]
---

# Aperiodic

**A state or class is aperiodic when returns are not locked into a nontrivial cycle.**

## Definition

The period of state $i$ is
$$
d(i)=\gcd\{n\geq 1:P_{ii}^{(n)}>0\}.
$$
State $i$ is aperiodic if $d(i)=1$.

## Key Properties

- Period is a class property: communicating states have the same period.
- A self-loop $P_{ii}>0$ implies aperiodicity for state $i$.
- Aperiodicity is needed for ordinary limits $P_{ij}^{(n)}$ to converge without oscillation.

## Intuition

If a class has period 2, the chain may alternate forever between even and odd times. Aperiodicity removes that clock-phase effect.

## Connection to Other Concepts

Aperiodicity is the extra condition that turns stationary probabilities into [[concepts/limiting-probability-distribution|Limiting Probability Distribution]] in positive recurrent classes.

## Theorems

- [[theorems/period-class-property|Period Is a Class Property]]
- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]

## Examples

- The deterministic two-state alternation has period 2 and no ordinary limiting distribution, even though it has a stationary distribution.

## Open Questions / Gaps

> [!todo] Gap - Add Cesaro-limit treatment for periodic chains.

## Sources

- [[sources/lecture-notes-ch3]] - periodicity and limiting behavior.
