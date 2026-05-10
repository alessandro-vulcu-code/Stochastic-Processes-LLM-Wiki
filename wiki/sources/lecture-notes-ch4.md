---
type: source
slug: lecture-notes-ch4
title: Chapter 4 - Poisson Processes
author: Unknown
date: 2020
source-type: lecture-notes
tags: [poisson-process, continuous-time, queueing]
ingested: 2026-05-10
---

# Chapter 4 - Poisson Processes

## Summary

This chapter gives a full treatment of the [[concepts/poisson-process|Poisson process]]. It begins with Poisson-distribution closure under sums and Bernoulli filtering, then defines the continuous-time process through independent stationary increments and Poisson-distributed counts.

It develops the law of rare events, superposition, thinning, inter-arrival and waiting-time distributions, and conditional arrival-time structure. Given $n$ arrivals in $(0,t)$, arrival times are distributed as ordered independent uniforms, which immediately yields binomial conditional counts in subintervals.

The chapter then turns to applied queueing and observation principles: [[concepts/m-g-infinity-queue|M/G/infinity]] style counting, shot noise, [[concepts/pasta|PASTA]], departure distributions in stable [[concepts/m-g-1-queue|M/G/1]] queues, periodic-class limits, and a large set of Poisson-process exercises.

## Key Concepts Introduced

- [[concepts/poisson-process|Poisson Process]] - independent stationary Poisson increments.
- [[concepts/non-homogeneous-poisson-process|Non-Homogeneous Poisson Process]] - time-varying intensity.
- [[concepts/pasta|PASTA]] - Poisson Arrivals See Time Averages.
- [[concepts/m-g-infinity-queue|M/G/infinity Queue]] - Poisson arrivals, general service, infinitely many servers.
- [[concepts/backward-recurrence-time|Backward Recurrence Time]] - age of an interval viewed from time $t$.
- [[concepts/poisson-distribution|Poisson Distribution]] - closed under sums and thinning.
- [[concepts/exponential-distribution|Exponential Distribution]] - inter-arrival times.
- [[concepts/gamma-distribution|Gamma Distribution]] - waiting time for the $n$-th arrival.

## Key Theorems

- [[theorems/poisson-sum|Sum of Independent Poisson Variables]].
- [[theorems/poisson-binomial-filter|Binomial Filter of a Poisson Variable]].
- [[theorems/poisson-approximation-bound|Poisson Approximation Bound]].
- [[theorems/superposition-theorem|Superposition Theorem]].
- [[theorems/thinning-theorem|Thinning Theorem]].
- [[theorems/poisson-interarrival-exponential|Poisson Inter-Arrivals Are Exponential]].
- [[theorems/waiting-times-gamma|Waiting Times Are Gamma]].
- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]].
- [[theorems/binomial-conditional-distribution|Binomial Conditional Distribution]].
- [[theorems/pasta|PASTA]].

## Notation

- $X(t)$ or $N(t)$ for the Poisson counting process.
- $\lambda$ for process rate.
- $S_i$ for inter-arrival times.
- $W_n$ for the $n$-th arrival time.

## Critique / Gaps

The chapter mixes theorem statements with many worked exercises. The major Chapter 4 exercise sequence has now been promoted into individual exercise pages; remaining work is mostly deeper polishing and any omitted OCR-damaged variants.

## Wiki Pages Updated

- [[concepts/poisson-process]], [[concepts/non-homogeneous-poisson-process]], [[concepts/pasta]], [[concepts/m-g-infinity-queue]], [[concepts/backward-recurrence-time]], [[concepts/poisson-distribution]], [[concepts/exponential-distribution]], [[concepts/gamma-distribution]]
- [[theorems/poisson-sum]], [[theorems/poisson-binomial-filter]], [[theorems/poisson-approximation-bound]], [[theorems/superposition-theorem]], [[theorems/thinning-theorem]], [[theorems/poisson-interarrival-exponential]], [[theorems/waiting-times-gamma]], [[theorems/conditional-arrival-times-uniform]], [[theorems/binomial-conditional-distribution]], [[theorems/pasta]]
- [[topics/poisson-processes]]
- [[exercises/undersea-cable-defects]], [[exercises/store-arrivals-poisson-increments]], [[exercises/radioactive-particles-m-g-infinity]], [[exercises/shot-noise-process-moments]], [[exercises/two-independent-poisson-processes]], [[exercises/finite-delay-line-markov-chain]], [[exercises/infinite-delay-line-chain]], [[exercises/fraction-transitions-between-states]], [[exercises/limits-regular-chain]], [[exercises/backward-probability]], [[exercises/man-with-cars]], [[exercises/periodic-class-general-limit]], [[exercises/shock-survival]], [[exercises/dispatching-system]], [[exercises/typographical-errors]], [[exercises/circular-disk-poisson-limit]], [[exercises/first-time-all-processes-fire]], [[exercises/batch-holding-facility]], [[exercises/mean-first-arrival-time-given-n]], [[exercises/mean-total-waiting-time-five-customers]], [[exercises/store-empty-end-hour]]
