---
type: source
slug: lecture-notes-ch5
title: Chapter 5 - Renewal Phenomena
author: Unknown
date: 2020
source-type: lecture-notes
tags: [renewal-process, regenerative-processes, semi-markov-processes]
ingested: 2026-05-10
---

# Chapter 5 - Renewal Phenomena

## Summary

This chapter generalizes the Poisson process to [[concepts/renewal-process|renewal processes]], where interoccurrence times are positive finite i.i.d. random variables with arbitrary distribution $F$. It defines renewal epochs $W_n$, the counting process $N(t)$, and the [[concepts/renewal-function|renewal function]] $M(t)=\mathbb{E}[N(t)]$.

The chapter develops [[concepts/excess-life|excess life]], [[concepts/backward-recurrence-time|current/backward recurrence time]], total life, the [[concepts/sampling-paradox|sampling paradox]], the [[concepts/renewal-equation|renewal equation]], elementary and basic renewal theorems, [[concepts/delayed-renewal-process|delayed]] and stationary renewal processes, [[concepts/alternating-renewal-process|alternating renewal processes]], and renewal reward processes. These results give long-run rates and time fractions from one-cycle expectations.

The final part uses renewal theory to prove the Markov-chain Basic Limit Theorem, then introduces [[concepts/regenerative-process|regenerative processes]] and [[concepts/semi-markov-process|semi-Markov processes]]. Semi-Markov processes inherit transition probabilities from an embedded Markov chain but attach random holding times to transitions; their real-time stationary distribution is proportional to embedded visit frequency times mean sojourn time.

## Key Concepts Introduced

- [[concepts/renewal-process|Renewal Process]] - counting process with i.i.d. interoccurrence times.
- [[concepts/renewal-function|Renewal Function]] - expected renewal count $M(t)$.
- [[concepts/excess-life|Excess Life]] - residual time to the next renewal.
- [[concepts/backward-recurrence-time|Backward Recurrence Time]] - age since the last renewal.
- [[concepts/sampling-paradox|Sampling Paradox]] - length-biased observation of renewal intervals.
- [[concepts/renewal-equation|Renewal Equation]] - recursive integral equation from conditioning on the first renewal.
- [[concepts/delayed-renewal-process|Delayed Renewal Process]] - first interval has a different distribution.
- [[concepts/alternating-renewal-process|Alternating Renewal Process]] - ON/OFF time fractions from cycle means.
- [[concepts/renewal-reward-process|Renewal Reward Process]] - reward accumulated per renewal cycle.
- [[concepts/regenerative-process|Regenerative Process]] - process that probabilistically restarts at regeneration times.
- [[concepts/semi-markov-process|Semi-Markov Process]] - embedded Markov chain plus random transition durations.

## Key Theorems

- [[theorems/elementary-renewal-theorem|Elementary Renewal Theorem]].
- [[theorems/basic-renewal-theorem|Basic Renewal Theorem]].
- [[theorems/finiteness-renewal-function|Finiteness of the Renewal Function]].
- [[theorems/solution-renewal-equation|Solution of the Renewal Equation]].
- [[theorems/basic-limit-theorem-renewal-proof|Basic Limit Theorem via Renewal Theory]].
- [[theorems/renewal-reward-theorem|Renewal Reward Theorem]].
- [[theorems/semi-markov-long-run-distribution|Semi-Markov Long-Run Distribution]].

## Notation

- $X_i$ for interoccurrence times.
- $W_n=X_1+\cdots+X_n$ for renewal epochs.
- $N(t)=\max(n:W_n\leq t)$ for renewal count.
- $M(t)=\mathbb{E}[N(t)]$ for renewal function.
- $\gamma_t$ for excess life, $\delta_t$ for current life, $\beta_t$ for total life.
- $\mu=\mathbb{E}[X]$ for mean interrenewal time.

## Critique / Gaps

Several renewal theorem proofs are stated without full proof in the source. The wiki marks these as source gaps and records the statements, interpretations, and conditions.

## Wiki Pages Updated

- [[concepts/renewal-process]], [[concepts/renewal-function]], [[concepts/excess-life]], [[concepts/backward-recurrence-time]], [[concepts/sampling-paradox]], [[concepts/renewal-equation]], [[concepts/delayed-renewal-process]], [[concepts/alternating-renewal-process]], [[concepts/renewal-reward-process]], [[concepts/regenerative-process]], [[concepts/semi-markov-process]]
- [[theorems/elementary-renewal-theorem]], [[theorems/basic-renewal-theorem]], [[theorems/finiteness-renewal-function]], [[theorems/solution-renewal-equation]], [[theorems/basic-limit-theorem-renewal-proof]], [[theorems/renewal-reward-theorem]], [[theorems/semi-markov-long-run-distribution]]
- [[topics/renewal-phenomena]]
- [[exercises/failure-wald-like-identity]], [[exercises/renewal-function-mean-variance]], [[exercises/sojourns-long-run-state1]], [[exercises/triangular-renewal-count]], [[exercises/excess-life-triangular-lifetime]], [[exercises/excess-life-uniform-lifetimes]], [[exercises/loss-system-poisson-arrivals]], [[exercises/two-component-parallel-system]], [[exercises/two-bulbs-half-lit-office]]
