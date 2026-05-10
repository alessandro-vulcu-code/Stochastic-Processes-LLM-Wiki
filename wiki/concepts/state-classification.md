---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[concepts/communicating-classes]], [[concepts/recurrence]], [[concepts/positive-recurrent]], [[concepts/null-recurrent]]
---

# State Classification

**State classification organizes Markov-chain states into transient, null recurrent, and positive recurrent behavior, with class and period structure layered on top.**

## Definition

The Ch3 classification asks, for each state or communicating class:

- Is it transient or recurrent?
- If recurrent, is it [[concepts/null-recurrent|Null Recurrent]] or [[concepts/positive-recurrent|Positive Recurrent]]?
- What is its [[concepts/period|Period]]?
- Is the class closed/recurrent or reachable only transiently?

## Key Properties

- Communication makes recurrence and period class properties.
- Closed finite classes are positive recurrent.
- Transient states eventually feed into recurrent classes when such classes are reachable.

## Intuition

Classification tells what the chain does after enough time: escape, cycle, settle into a positive long-run law, or return forever with vanishing occupation mass.

## Connection to Other Concepts

This page ties together [[concepts/irreducible|Irreducible]], [[concepts/aperiodic|Aperiodic]], [[concepts/recurrence|Recurrence]], and [[concepts/limiting-probability-distribution|Limiting Probability Distribution]].

## Theorems

- [[theorems/recurrence-criterion|Recurrence Criterion]]
- [[theorems/transience-criterion|Transience Criterion]]
- [[theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]]

## Examples

- Random walks with variable parameters are classified by convergence of products of local odds ratios.
- The M/G/1 queue has positive recurrent, null recurrent, and transient regimes depending on $\rho$.

## Open Questions / Gaps

> [!todo] Gap - Add a classification decision tree as a query-generated page.

## Sources

- [[sources/lecture-notes-ch3]] - summary tables and examples.
