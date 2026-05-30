---
type: source
slug: stochastic-exercises-guida-semplice
title: Stochastic Exercises - Guida Semplice
author: Sergio Cibecchini
date: 2025-06-16
source-type: lecture-notes
tags: [markov-chains, poisson-process, renewal-process, gobackn-protocol, queueing, exercises]
ingested: 2026-05-27
---

# Stochastic Exercises - Guida Semplice

## Summary

This source is a compact exam-method PDF for Stochastic Processes, marked as AA 2024/2025 and authored by Sergio Cibecchini. It is an annotated solution guide rather than a theory text: the pages show which computational pattern to use for recurring exam exercise families.

The first block covers GoBackN throughput over a two-state Markov channel. The practical workflow is: build the channel transition matrix, solve the stationary good/bad probabilities, use direct throughput $\eta=\pi_{\text{good}}$ without retransmission, and use $m$-step transition probabilities for GoBackN with round-trip delay $m$. It also records variants with iid feedback errors and alternating Markov/iid channel phases.

The middle block focuses on renewal/reward and queueing templates: one-server and two-server attack/recovery cycles, long-run no-service fractions, intervention rates, average traffic reward per cycle, M/G/infinity active-population counts, and finite-window survival probabilities. The source repeatedly converts an event process into a cycle or a Poisson thinning/survival calculation.

The final block covers finite Markov-chain exercises and Poisson conditioning. It gives templates for row-vector propagation $e_iP^n$, stationary/limiting distributions, reducible chains with transient states and recurrent classes, expected visit counts before absorption, mean absorption time, conditional probabilities along Markov paths, and case distinctions for two independent Poisson processes when the conditioning interval is past, future, or the same interval.

## Key Concepts Introduced

- [[wiki/concepts/gobackn-protocol]] - practical throughput formulas from channel matrix powers and feedback-error variants.
- [[wiki/concepts/renewal-reward-process]] - cycle reward/time ratios for network attack and recovery models.
- [[wiki/concepts/regenerative-process]] - restart cycles used to compute long-run availability and intervention rates.
- [[wiki/concepts/m-g-infinity-queue]] - active-customer counts as Poisson variables with mean $\lambda\int_0^t \overline G(y)\,dy$.
- [[wiki/concepts/poisson-process]] - arrivals, thinning, independent increments, and conditional split formulas.
- [[wiki/concepts/conditional-probability]] - Markov path conditioning and Poisson interval conditioning.
- [[wiki/concepts/absorbing-markov-chain]] - transient-to-absorbing calculations.
- [[wiki/concepts/fundamental-matrix]] - expected visits and mean absorption time.
- [[wiki/concepts/state-classification]] - closed recurrent classes, transient states, periodicity, and aperiodicity.
- [[wiki/concepts/limiting-probability-distribution]] - ordinary limits versus Cesaro averages in reducible/periodic chains.

## Key Theorems

- [[wiki/theorems/gobackn-throughput-markov-errors]] - throughput formulas for Markov errors and feedback-error variants.
- [[wiki/theorems/renewal-reward-theorem]] - long-run fractions and average traffic from renewal cycles.
- [[wiki/theorems/conditional-arrival-times-uniform]] - arrivals conditioned on a Poisson count are uniform over the interval.
- [[wiki/theorems/binomial-conditional-distribution]] - subinterval or stream counts given a total count.
- [[wiki/theorems/poisson-binomial-filter]] - active populations and surviving arrivals via thinning.
- [[wiki/theorems/fundamental-matrix]] - expected visits before absorption.
- [[wiki/theorems/mean-absorption-time]] - row sums of the expected-visit matrix.
- [[wiki/theorems/mean-first-passage-time]] - first-step equations for hitting times.
- [[wiki/theorems/transient-to-recurrent-limit]] - reducible-chain limits through recurrent-class absorption.

## Notation

- The source uses states $0,1$ for good/bad channel states in the GoBackN examples.
- The source writes $\pi$ informally as "pi greco" for stationary probabilities.
- $T_0,T_1,T_2$ denote mean attack-arrival time, cleanup time, and manual repair time in renewal-cycle examples.
- In M/G/infinity examples, $\lambda_{pt}$ denotes the time-dependent Poisson mean
  $$
  \lambda_{pt}=\lambda\int_0^t [1-G(y)]\,dy.
  $$
- The source alternates between $X_n$ for discrete-time Markov chains and $X(t)$ for Poisson/queueing counts.

## Critique / Gaps

This source is intentionally terse. It is strong for recognition and setup, but many algebraic steps are handwritten and some numeric substitutions are not fully explained. The PDF has a sparse text layer, so formulas were checked visually from rendered pages. The wiki page created from it keeps the robust templates and avoids relying on unclear handwriting where the same method is already covered by lecture-note sources.

## Wiki Pages Updated

- [[wiki/exercises/stochastic-exercises-guida-semplice]]
- [[wiki/concepts/gobackn-protocol]]
- [[wiki/concepts/renewal-reward-process]]
- [[wiki/concepts/m-g-infinity-queue]]
- [[wiki/concepts/poisson-process]]
- [[wiki/concepts/conditional-probability]]
- [[wiki/concepts/absorbing-markov-chain]]
- [[wiki/concepts/fundamental-matrix]]
- [[wiki/concepts/state-classification]]
- [[wiki/concepts/limiting-probability-distribution]]
- [[wiki/theorems/renewal-reward-theorem]]
- [[wiki/theorems/fundamental-matrix]]
- [[wiki/theorems/mean-absorption-time]]
- [[wiki/theorems/mean-first-passage-time]]
- [[wiki/theorems/binomial-conditional-distribution]]
- [[wiki/theorems/two-processes-conditional-distribution]]
- [[wiki/theorems/transient-to-recurrent-limit]]
- [[wiki/theorems/gobackn-throughput-markov-errors]]
- [[wiki/topics/gobackn-protocol]]
- [[wiki/topics/renewal-phenomena]]
- [[wiki/topics/poisson-processes]]
- [[wiki/topics/markov-chains]]
- [[wiki/topics/long-run-behaviour]]
- [[wiki/overview]]
