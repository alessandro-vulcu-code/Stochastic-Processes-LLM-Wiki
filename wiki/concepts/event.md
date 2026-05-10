---
type: concept
tags: [stochastic-processes, probability, measure-theory]
sources: [lecture-notes-ch1]
related: [[concepts/sample-space]], [[concepts/conditional-probability]], [[concepts/independence-of-rvs]]
---

# Event

**An event is an observable subset of the sample space to which a probability can be assigned.**

## Definition

Given a probability space $(\Omega,\mathcal{F},\mathbb{P})$, an event is a set $A\in\mathcal{F}$. Its probability is $\mathbb{P}(A)$.

## Key Properties

- Events can be combined using set operations: $A\cap B$, $A\cup B$, and $A^c$.
- Conditional probability is defined by $\mathbb{P}(A\mid B)=\mathbb{P}(A\cap B)/\mathbb{P}(B)$ when $\mathbb{P}(B)>0$.
- Events $A_1,\ldots,A_n$ are independent when probabilities of finite intersections factor.

## Intuition

An event is a yes/no question about the outcome. For a process, typical events are path statements such as $\{X(t)=k\}$ or $\{\tau_i<\infty\}$.

## Connection to Other Concepts

Events are the objects manipulated by [[concepts/conditional-probability|Conditional Probability]] and by the independence assumptions behind [[concepts/poisson-process|Poisson Process]] increments.

## Theorems

- [[theorems/law-of-total-probability|Law of Total Probability]]

## Examples

- $\{X\leq x\}$ for a random variable $X$.
- $\{X(t+h)-X(t)=1\}$ for a counting process.

## Open Questions / Gaps

> [!todo] Gap - Add sigma-algebra closure properties if later notes require formal measure theory.

## Sources

- [[sources/lecture-notes-ch1]] - event probability, conditioning, and independence review.
