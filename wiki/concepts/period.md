---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch3, lecture-notes-ch4]
related: [communicating-classes, basic-limit-theorem]
---

# Period

**The period of a state is the greatest common divisor of possible return times to that state.**

## Definition

For state $i$,
$$
d(i)=\gcd\{n\geq 1:P_{ii}^{(n)}>0\}.
$$
If $d(i)=1$, the state is aperiodic.

## Key Properties

- Period is a class property.
- $P_{ii}>0$ implies $d(i)=1$.
- Ordinary limiting probabilities may oscillate in periodic classes.
- Cesaro averages can still converge when ordinary limits do not.

## Intuition

Period measures whether returns to a state are locked onto a cycle.

## Connection to Other Concepts

- [[communicating-classes]] share period.
- [[basic-limit-theorem]] requires aperiodicity for ordinary limits.

## Theorems

- [[period-class-property]]
- [[basic-limit-theorem]]

## Examples

- A deterministic cycle through $N$ states has period $N$.
- A two-state alternating class has period 2.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch3]] - definition and class theorem.
- [[sources/lecture-notes-ch4]] - periodic-class limit remarks.

