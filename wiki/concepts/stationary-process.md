---
type: concept
tags: [stochastic-processes, stationarity]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [[concepts/stochastic-process]], [[concepts/poisson-process]], [[concepts/homogeneous-markov-chain]]
---

# Stationary Process

**A stationary process has probability laws that do not change under shifts of the time origin.**

## Definition

In the broad sense used in the notes, a process is called stationary if the relevant distributional behavior is invariant in time. Chapter 1 states the simplest version: if all $X_t$ share the same distribution, the process is stationary.

For increments, stationary increments mean
$$
X(t+s)-X(s)\stackrel{d}{=}X(t)-X(0),
$$
so the increment law depends only on interval length.

## Key Properties

- Stationarity reduces the amount of distributional information needed to specify a process.
- A [[concepts/poisson-process|Poisson Process]] has stationary increments.
- A [[concepts/homogeneous-markov-chain|Homogeneous Markov Chain]] has time-independent transition probabilities.

## Intuition

Stationarity says that the clock label itself should not matter. What matters is duration, state, or relative position.

## Connection to Other Concepts

Stationarity is distinct from [[concepts/stationary-distribution|Stationary Distribution]]: the former is a property of a process law over time, while the latter is an invariant probability vector for a Markov chain.

## Theorems

- [[theorems/poisson-interarrival-exponential|Poisson Inter-Arrivals Are Exponential]]

## Examples

- Poisson increments over any interval of length $t$ have Poisson$(\lambda t)$ law.
- A time-homogeneous Markov chain uses the same transition matrix at every step.

## Open Questions / Gaps

> [!todo] Gap - Refine weak/strict stationarity if a later source introduces covariance-stationary processes.

## Sources

- [[sources/lecture-notes-ch1]] - initial definition for stochastic processes.
- [[sources/lecture-notes-ch4]] - stationary increments of Poisson processes.
