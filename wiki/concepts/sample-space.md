---
type: concept
tags: [stochastic-processes, probability, measure-theory]
sources: [lecture-notes-ch1]
related: [[concepts/event]], [[concepts/random-variable]], [[concepts/conditional-probability]]
---

# Sample Space

**The sample space $\Omega$ is the set of all possible outcomes of a random experiment.**

## Definition

A probabilistic model starts from a triple $(\Omega,\mathcal{F},\mathbb{P})$, where $\Omega$ is the sample space, $\mathcal{F}$ is a collection of observable events, and $\mathbb{P}$ assigns probabilities to those events.

## Key Properties

- Outcomes $\omega\in\Omega$ are elementary realizations of the experiment.
- [[concepts/event|Events]] are subsets of $\Omega$ that belong to $\mathcal{F}$.
- A [[concepts/random-variable|Random Variable]] is a measurable map from $\Omega$ to a numerical state space.

## Intuition

$\Omega$ is the hidden universe in which randomness lives. In stochastic processes, one outcome $\omega$ usually determines an entire sample path $t\mapsto X_t(\omega)$.

## Connection to Other Concepts

The sample space supports [[concepts/stochastic-process|Stochastic Process]] paths and makes definitions such as [[concepts/independence-of-rvs|Independence of Random Variables]] precise.

## Theorems

- [[theorems/law-of-total-probability|Law of Total Probability]]

## Examples

- Tossing a coin once: $\Omega=\{H,T\}$.
- A Poisson-process path: $\Omega$ can be the set of all nondecreasing integer-valued counting paths.

## Open Questions / Gaps

> [!todo] Gap - Add a measure-theoretic construction page if later sources introduce sigma-algebras formally.

## Sources

- [[sources/lecture-notes-ch1]] - implicit probability-space foundation for random variables and processes.
