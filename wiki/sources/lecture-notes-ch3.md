---
type: source
slug: lecture-notes-ch3
title: Chapter 3 - Long Run Behaviour of Markov Chains
author: Unknown
date: 2020
source-type: lecture-notes
tags: [markov-chains, recurrence, ergodic-theory]
ingested: 2026-05-10
---

# Chapter 3 - Long Run Behaviour of Markov Chains

## Summary

This chapter studies asymptotic Markov-chain behaviour. It begins with regular finite chains and their [[concepts/limiting-probability-distribution|limiting distributions]], then generalizes through accessibility, communication, [[concepts/irreducible|irreducibility]], periodicity, recurrence, [[concepts/positive-recurrent|positive recurrence]], [[concepts/null-recurrent|null recurrence]], and transience.

The central result is the [[theorems/basic-limit-theorem|Basic Limit Theorem]]: for recurrent irreducible aperiodic chains or classes, $P_{ji}^{(n)}\to \pi_i=1/m_i$, where $m_i$ is the mean return time to state $i$. The chapter also treats reducible chains by decomposing limits into absorption probabilities into recurrent classes and limiting distributions inside those classes.

The final part develops transience criteria for irreducible chains on $\mathbb{N}$ using bounded solutions of harmonic equations, then applies the criteria to variable random walks and the M/G/1 embedded chain. The M/G/1 classification is positive recurrent for $\rho<1$, null recurrent for $\rho=1$, and transient for $\rho>1$.

## Key Concepts Introduced

- [[concepts/communicating-classes|Communicating Classes]] - equivalence classes under mutual accessibility.
- [[concepts/irreducible|Irreducible]] - one communicating class.
- [[concepts/period|Period]] - gcd of possible return times.
- [[concepts/aperiodic|Aperiodic]] - period one, so ordinary limits can exist.
- [[concepts/recurrence|Recurrence]] - recurrent, transient, positive recurrent, and null recurrent states.
- [[concepts/positive-recurrent|Positive Recurrent]] - finite mean return time.
- [[concepts/null-recurrent|Null Recurrent]] - recurrent with infinite mean return time.
- [[concepts/state-classification|State Classification]] - transient/null/positive recurrent and periodic structure.
- [[concepts/stationary-distribution|Stationary Distribution]] - solution of $\pi=\pi P$.
- [[concepts/limiting-probability-distribution|Limiting Probability Distribution]] - limit of $P_{ij}^{(n)}$.
- [[concepts/random-walk|Random Walk]] - recurrence/transience classification by local odds products.

## Key Theorems

- [[theorems/limiting-distribution-regular-markov-chain|Limiting Distribution of a Regular Markov Chain]].
- [[theorems/period-class-property|Period Is a Class Property]].
- [[theorems/basic-limit-theorem|Basic Limit Theorem]].
- [[theorems/recurrence-criterion|Recurrence Criterion]].
- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]].
- [[theorems/finite-state-positive-recurrence|Finite-State Positive Recurrence Facts]].
- [[theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]].
- [[theorems/transience-criterion|Transience Criterion]].

## Notation

- $i\leftrightarrow j$ for communication.
- $d(i)=\gcd\{n\geq 1:P_{ii}^{(n)}>0\}$ for period.
- $f_{ii}^{(n)}$ for first return at time $n$.
- $m_i=\sum_{n\geq 1}n f_{ii}^{(n)}$ for mean return time.
- $\pi_i(C)$ for probability of eventual absorption into recurrent class $C$.

## Critique / Gaps

Some theorem proofs are only sketched or deferred to renewal theory in Chapter 5. The notes contain several OCR-damaged tables, so the wiki records the stable formulas rather than reproducing malformed table layouts.

## Wiki Pages Updated

- [[concepts/communicating-classes]], [[concepts/irreducible]], [[concepts/period]], [[concepts/aperiodic]], [[concepts/recurrence]], [[concepts/positive-recurrent]], [[concepts/null-recurrent]], [[concepts/state-classification]], [[concepts/stationary-distribution]], [[concepts/limiting-probability-distribution]], [[concepts/random-walk]]
- [[theorems/limiting-distribution-regular-markov-chain]], [[theorems/period-class-property]], [[theorems/basic-limit-theorem]], [[theorems/recurrence-criterion]], [[theorems/stationary-distribution-positive-recurrent-aperiodic]], [[theorems/stationary-distribution-positive-recurrent-class]], [[theorems/finite-state-positive-recurrence]], [[theorems/transient-to-recurrent-limit]], [[theorems/transience-criterion]]
- [[topics/long-run-behaviour]]
- [[exercises/urn-removal-mean-duration]], [[exercises/last-toss-coins-absorption]], [[exercises/g-m-1-positive-recurrence]], [[exercises/random-walk-variable-parameters]], [[exercises/m-g-1-classification]]
