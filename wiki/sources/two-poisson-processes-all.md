---
type: source
slug: two-poisson-processes-all
title: Two Poisson Processes All
author: Unknown
date: 2026-06-07
source-type: lecture-notes
tags: [poisson-process, conditional-probability, exam-prep]
ingested: 2026-06-07
---

# Two Poisson Processes All

## Summary

This source is a compact collection of exam prompts about two independent Poisson processes. The repeated pattern is conditional probability with overlapping time intervals, combined counts, and partial information about one process.

The main computational method is to split each process into disjoint time increments, use independence of increments and independence between processes, then reduce the problem to a Poisson, binomial, multinomial, or small Bayes-ratio calculation.

Together with [[stochastic-exercises-guida-semplice]], this source motivates a dedicated formulario page for "two Poisson processes" exercises.

## Key Concepts Introduced

- [[concepts/poisson-process]] - independent stationary increments and Poisson count laws.
- [[concepts/conditional-probability]] - conditioning on totals, subinterval counts, and partial counts.

## Key Theorems

- [[theorems/superposition-theorem]] - sums of independent Poisson processes are Poisson.
- [[theorems/two-processes-conditional-distribution]] - conditional split between two independent Poisson processes is binomial.
- [[theorems/binomial-conditional-distribution]] - conditional split across subintervals is binomial.
- [[theorems/conditional-arrival-times-uniform]] - given a count in an interval, arrivals are uniformly located inside the interval.

## Notation

- $X_i(t)$ counts arrivals of process $i$ in $[0,t]$.
- $N_i(a,b]=X_i(b)-X_i(a)$ counts arrivals of process $i$ in $(a,b]$.
- $N_i(a,b]\sim\operatorname{Poisson}(\lambda_i(b-a))$.

## Critique / Gaps

The source is a prompt collection rather than a full solution manual. Several exercises are duplicated with changed rates or time horizons. The useful contribution is the taxonomy of recurring conditional-probability cases.

## Wiki Pages Updated

- [[exercises/two-poisson-processes-formulario]]

