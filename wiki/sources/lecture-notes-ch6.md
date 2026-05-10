---
type: source
slug: lecture-notes-ch6
title: Chapter 6 - Analysis of the GoBackN Protocol
author: Unknown
date: 2020
source-type: lecture-notes
tags: [gobackn, semi-markov-processes, renewal-reward]
ingested: 2026-05-10
---

# Chapter 6 - Analysis of the GoBackN Protocol

## Summary

This chapter applies Markov-chain, semi-Markov, and renewal-reward ideas to [[concepts/gobackn-protocol|GoBackN protocol]] throughput. The protocol accepts packets only in order; after a bad packet, the sender retransmits from the corrupted packet and the next $m-1$ slots are skipped from the protocol's throughput-opportunity perspective.

The first part builds semi-Markov reward models for Markov packet errors with error-free feedback, bidirectional Markov errors, i.i.d. feedback errors, and equivalent reduced state models. Throughput is consistently a reward/time ratio: expected accepted packets per expected physical slot.

The second part develops a transform method for counting Markov-chain rewards. A transition-generating matrix $\psi(\vec{s})$ packages transition probabilities and metric values; setting $\vec{s}=1$ recovers the embedded transition matrix, while derivatives at $\vec{s}=1$ recover average reward and time vectors. This gives a compact method for protocol throughput.

## Key Concepts Introduced

- [[concepts/gobackn-protocol|GoBackN Protocol]] - retransmit from first corrupted packet; accepted in-order throughput.
- [[concepts/transition-generating-matrix|Transition Generating Matrix]] - matrix generating function for transition metrics.
- [[concepts/semi-markov-process|Semi-Markov Process]] - protocol state plus state-dependent time durations.
- [[concepts/renewal-reward-process|Renewal Reward Process]] - throughput as reward divided by time.

## Key Theorems

- [[theorems/gobackn-throughput-markov-errors|GoBackN Throughput with Markov Errors]].
- [[theorems/transition-generating-matrix-method|Transition Generating Matrix Method]].

## Notation

- $m$ for round-trip time in slots.
- $G$ / $B$ for good and bad sampled channel states.
- $R_i$ for reward in state $i$.
- $T_i$ for time consumed by state $i$.
- $\eta$ for throughput.
- $\psi(s_1,s_2)$ for transition generating matrix with reward and time metrics.

## Critique / Gaps

Some transition matrices in the raw source have OCR issues or missing columns. The wiki preserves the stable throughput formulas and conceptual modeling steps, not every damaged matrix entry.

## Wiki Pages Updated

- [[concepts/gobackn-protocol]], [[concepts/transition-generating-matrix]], [[concepts/semi-markov-process]], [[concepts/renewal-reward-process]]
- [[theorems/gobackn-throughput-markov-errors]], [[theorems/transition-generating-matrix-method]]
- [[topics/gobackn-protocol]]
- [[exercises/gobackn-transform-throughput]]

