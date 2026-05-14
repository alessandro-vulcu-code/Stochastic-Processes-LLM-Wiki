---
type: source
slug: how-to-stochastic-processes
title: How To Stochastic Processes
author: Unknown
date: 2024-06-30
source-type: lecture-notes
tags: [markov-chains, poisson-process, renewal-process, gobackn-protocol, exercises]
ingested: 2026-05-14
---

# How To Stochastic Processes

## Summary

This source is a practical handwritten exam-preparation document, transcribed in `raw/How To Stochastic Processes _240630_183444 (1).md` from the corresponding PDF. It collects the recurring computational templates for the Stochastic Processes exam: finite Markov chains, Go-Back-N throughput, Poisson-process conditioning, M/G/infinity-style active-customer counts, and renewal/reward cycles.

Its value is operational rather than theoretical: it shows which formula is normally applied in each exam pattern. The enriched wiki version clarifies omitted steps, fixes ambiguous points where the transcription appears inconsistent, and links the procedures to the relevant wiki theorems.

## Key Concepts Introduced

- [[wiki/concepts/markov-chain]] - steady-state probabilities, first passage, expected visits, and absorbing cases.
- [[wiki/concepts/poisson-process]] - conditional counts, superposition, thinning, and active-population examples.
- [[wiki/concepts/renewal-process]] - renewal cycles and long-run time fractions.
- [[wiki/concepts/renewal-reward-process]] - average delay and throughput as reward/time ratios.
- [[wiki/concepts/gobackn-protocol]] - throughput formulas for Markov and iid error models.

## Key Theorems

- [[wiki/theorems/mean-first-passage-time]] - first-step equations for hitting times.
- [[wiki/theorems/fundamental-matrix]] - expected visits before absorption.
- [[wiki/theorems/binomial-conditional-distribution]] - Poisson subinterval counts given a total.
- [[wiki/theorems/superposition-theorem]] - sum of independent Poisson streams.
- [[wiki/theorems/thinning-theorem]] - filtering/marking Poisson arrivals.
- [[wiki/theorems/renewal-reward-theorem]] - long-run averages by cycle rewards.
- [[wiki/theorems/gobackn-throughput-markov-errors]] - Go-Back-N throughput formulas.

## Notation

- The source alternates between state numbering from 0 and from 1. The enriched page states the convention locally.
- The source uses $d$, $\lambda$, and sometimes $\mu$ for Poisson rates; the enriched page standardizes rates as $\lambda$ when explaining the method.
- Some handwritten numeric values are ambiguous. The enriched page preserves the exercise type but flags corrections where needed.

## Critique / Gaps

The source sometimes writes final formulas without explaining why the conditioning event can be reduced, especially in Poisson exercises. It also contains a few likely transcription/manuscript errors: the second moment of first-passage time, one conditional two-link probability statement, and the final CSMA throughput value.

## Wiki Pages Updated

- [[wiki/exercises/how-to-stochastic-processes-enriched]]
- [[wiki/exercises/how-to-stochastic-processes-complete-en]]
