---
type: source
slug: exams-theorems
title: Exams Theorems
author: Course exam preparation list
date: 2026-05-23
source-type: article
tags: [exam-prep, markov-chains, poisson-process, renewal-process]
ingested: 2026-05-23
---

# Exams Theorems

## Summary

This source is a list of twelve theorem-style questions likely to appear on the stochastic-processes exam. It is not a primary mathematical source; it is a prioritization list for revision. The questions focus on finite-state recurrence, Chapman-Kolmogorov equations, period and recurrence as class properties, Poisson-process conditional distributions and interarrival times, reflected random walks on $\mathbb{N}$, and renewal-process limit identities.

The proofs in the corresponding exam-preparation page are assembled from the existing lecture-note wiki layer, especially Chapter 3 for Markov-chain classification, Chapter 4 for Poisson processes, and Chapter 5 for renewal theory.

## Key Concepts Introduced

- [[concepts/markov-chain|Markov Chain]] - finite-state and communicating-class arguments.
- [[concepts/recurrence|Recurrence]] - recurrent, transient, positive recurrent, and null recurrent states.
- [[concepts/period|Period]] - class property proof.
- [[concepts/poisson-process|Poisson Process]] - conditional count laws and exponential interarrival times.
- [[concepts/renewal-process|Renewal Process]] - renewal count, renewal epochs, and asymptotic renewal rate.
- [[concepts/renewal-function|Renewal Function]] - $M(t)=\mathbb{E}[N(t)]$.

## Key Theorems

- [[theorems/finite-state-positive-recurrence|Finite-State Positive Recurrence Facts]] - used for absence of null recurrence in finite chains.
- [[theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]] - multi-step transition decomposition.
- [[theorems/period-class-property|Period Is a Class Property]] - communicating states have common period.
- [[theorems/binomial-conditional-distribution|Binomial Conditional Distribution]] - conditional Poisson subinterval counts.
- [[theorems/poisson-interarrival-exponential|Poisson Inter-Arrivals Are Exponential]] - Poisson process as an exponential renewal process.
- [[theorems/elementary-renewal-theorem|Elementary Renewal Theorem]] - $M(t)/t\to 1/\mu$.

## Notation

- $X(t)$ denotes a Poisson counting process in the exam list.
- $X_n$ denotes renewal interarrival times in the renewal-process proofs.
- $S_n=X_1+\cdots+X_n$ denotes renewal epochs in the exam-preparation page.
- $N(t)=\max\{n:S_n\leq t\}$ and $M(t)=\mathbb{E}[N(t)]$.

## Critique / Gaps

Prompt 2 and prompt 10 ask for the same renewal identity in the earlier exam-theorem list, so the exam-preparation pages give two complementary proofs: a renewal-equation proof and a Wald stopping-time proof. The `raw/Theorems.md` version preserves a numbering jump from 9 to 11; the beginner-enriched page keeps that numbering and expands every proof step without changing the source variable names unnecessarily.

## Wiki Pages Updated

- [[exercises/exam-theorem-proofs]]
- [[exercises/exam-theorem-proofs-v2]]
- [[exercises/theorems-beginner-enriched]]
- [[sources/exams-theorems]]
