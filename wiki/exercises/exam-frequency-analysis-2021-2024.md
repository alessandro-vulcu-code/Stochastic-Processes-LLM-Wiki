---
type: exercise
tags: [exercise, exams, frequency-analysis, stochastic-processes]
sources: [raw-exams-2021-2024]
related: [gobackn-protocol, poisson-process, markov-chain, renewal-process, renewal-reward-process]
---

# Exam Frequency Analysis 2021-2024

This page cross-checks the exam files under `raw/Exams` and groups recurring exercises and proof prompts by template.

## Audit Notes

- Scope counted: exam sessions from 2021 to 2024 found under `raw/Exams/2021`, `raw/Exams/2022`, `raw/Exams/2023`, and `raw/Exams/2024`.
- Frequency unit: one exam session or track variant. Different tracks on the same date, such as ICT and Cybersecurity on 2024-07-01, are counted separately when the problem text differs.
- Duplicates merged: `raw/Exams/2021/22 june 2021.jpg` is a crop of the 2021-06-22 paper; `raw/Exams/2023/3 july 2023.jpg` and `raw/Exams/2023/3 july 2023.pdf` are the same paper; `raw/Exams/24-06-22.pdf` duplicates the 2022-06-24 paper.
- Excluded from frequency counts: `raw/Exams/mod20170713.pdf`, because it is a 2017 model/old exam outside the requested four-year window.
- Part B limitation: official Part B pages are available for 2021-06-22, 2021-07-13, 2022-06-24, 2024-02-23, and 2024-07-01 ICT. The 2024-07-01 Cybersecurity PDF also contains handwritten solution pages that reveal the same T1/T2/T3 prompts; those are marked as inferred, not official-text occurrences.

## Counted Sessions

| Date | Year label | Track | Source files counted |
|---|---|---|---|
| 2021-06-22 | AY 2020/2021 | Cybersecurity | `raw/Exams/2021/June 22, 2021 Cyber.pdf` |
| 2021-07-13 | AY 2020/2021 | Cybersecurity | `raw/Exams/2021/July 13, 2021 Cyber.pdf` |
| 2022-06-24 | AY 2021/2022 | General | `raw/Exams/2022/June 24, 2022.pdf` |
| 2023-06-16 | AY 2021/2022 as printed | General | `raw/Exams/2023/june 16 2023.pdf` |
| 2023-07-03 | AY 2022/2023 | General | `raw/Exams/2023/3 july 2023.pdf` and duplicate JPG |
| 2024-02-23 | AY 2022/2023 | General | `raw/Exams/2024/feb 23 2024.jpg`, `raw/Exams/2024/feb 23 2024-B.jpg` |
| 2024-06-12 | AY 2023/2024 | General/Cyber-style scan | `raw/Exams/2024/june 12 2024.jpg` |
| 2024-07-01 | AY 2023/2024 | ICT | `raw/Exams/2024/July 1, 2024 - ITC.pdf` |
| 2024-07-01 | AY 2023/2024 | Cybersecurity | `raw/Exams/2024/July 1, 2024 Cyber.pdf` |
| 2024-07-15 | AY 2023/2024 | Cybersecurity | `raw/Exams/2024/July 15, 2024 Cyber-1.jpg`, `raw/Exams/2024/July 15, 2024 Cyber-2.jpg` |

## Frequency Summary

| Rank | Exercise or proof family | Frequency | Notes |
|---:|---|---:|---|
| 1 | Go-Back-N throughput over a two-state Markov channel | 10 | Appears in every counted Part A paper. |
| 2 | Finite Markov-chain matrix analysis | 10 | Split into five-state classification/asymptotics (7) and three-state absorbing-chain evolution (3). |
| 3 | Renewal/reward availability applications | 10 | Split into single-node cleanup/manual-restore model (5) and two-server attacked streaming node (5). |
| 4 | Conditional probabilities for two independent Poisson processes | 9 | Appears in almost every Part A paper except 2021-07-13. |
| 5 | Renewal-process limit $\lim_{t\to\infty} N(t)/t$ | 4 official, 5 with inferred Cyber 2024-07-01 | Most frequent proof prompt. |
| 6 | Recurrence preserved across communicating states | 3 official, 4 with inferred Cyber 2024-07-01 | Markov-chain recurrence theorem. |
| 7 | Poisson interarrival times are iid exponential | 3 official, 4 with inferred Cyber 2024-07-01 | Core Poisson-process theorem. |
| 8 | Conditional distribution of Poisson counts given a total count | 2 | Appears in Part B on 2021-06-22 and 2022-06-24. |

## Exercise Families

## Go-Back-N Throughput over a Two-State Markov Channel

Frequency: 10.

Related pages: [[wiki/concepts/gobackn-protocol]], [[wiki/exercises/gobackn-transform-throughput]], [[wiki/theorems/gobackn-throughput-markov-errors]].

### 2021-06-22, AY 2020/2021, E2

Frequency: 10.

> Consider a two-state Markov channel, where the steady-state probability that the channel is in the bad state is 0.02 and the average number of consecutive good slots is 100. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2021-07-13, AY 2020/2021, E1

Frequency: 10.

> Consider a Go-Back-N protocol over a two-state Markov channel, where the average number of consecutive good slots is 100 and the average number of consecutive bad slots is $100/9$. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ will be retransmitted in slot $t + 2$.
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of the Go-Back-N protocol for an error-free feedback channel.
>
> (c) Compute the throughput of the Go-Back-N protocol for a feedback channel subject to iid errors with probability 0.1.

### 2022-06-24, AY 2021/2022, E2

Frequency: 10.

> Consider a two-state Markov channel, where the average number of consecutive good slots is 100 and the average number of consecutive bad slots is $100/49$. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2023-06-16, AY 2021/2022 as printed, E2

Frequency: 10.

> Consider a two-state Markov channel, where the average number of consecutive good slots is 100 and the average number of consecutive bad slots is $100/49$. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2023-07-03, AY 2022/2023, E1

Frequency: 10.

> Consider a Go-Back-N protocol over a two-state Markov channel, where the average number of consecutive good slots is 100 and the average fraction of bad slots is 0.1. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ will be retransmitted in slot $t + 2$.
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of the Go-Back-N protocol for an error-free feedback channel.
>
> (c) Compute the throughput of the Go-Back-N protocol for a feedback channel subject to iid errors with probability 0.1.

### 2024-02-23, AY 2022/2023, E1

Frequency: 10.

> Consider a Go-Back-N protocol over a two-state Markov channel, where the average number of consecutive good slots is 100 and the average fraction of bad slots is 0.1. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ will be retransmitted in slot $t + 2$.
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2024-06-12, AY 2023/2024, E2

Frequency: 10.

> Consider a two-state Markov channel, where the channel transition probability from the good state to itself is 0.95 and the average number of consecutive bad slots is 5. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2024-07-01, ICT, AY 2023/2024, E2

Frequency: 10.

> Consider a two-state Markov channel, where the channel transition probability from the good state to itself is 0.95 and the average number of consecutive bad slots is 5. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2024-07-01, Cybersecurity, AY 2023/2024, E1

Frequency: 10.

> Consider a two-state Markov channel, where the average probability of a bad channel is 0.1 and the average number of consecutive good slots is 20. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

### 2024-07-15, Cybersecurity, AY 2023/2024, E2

Frequency: 10.

> Consider a two-state Markov channel, where the channel transition probability from the good state to itself is 0.95 and the average number of consecutive bad slots is 5. The packet error probability is 1 for a bad slot and 0 for a good slot, respectively. The round-trip time is $m = 2$ slots, i.e., a packet that is erroneous in slot $t$ is retransmitted in slot $t + 2$ (if a retransmission protocol is used).
>
> (a) Compute the throughput that could be obtained if packets were directly transmitted over the channel without using any protocol.
>
> (b) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, in the presence of an error-free feedback channel.
>
> (c) Compute the throughput of a Go-Back-N protocol that transmits packets over the Markov channel described above, with a feedback channel subject to iid errors with probability $\delta = 0.1$.

## Conditional Probabilities for Two Independent Poisson Processes

Frequency: 9.

Related pages: [[wiki/concepts/poisson-process]], [[wiki/theorems/binomial-conditional-distribution]], [[wiki/theorems/superposition-theorem]], [[wiki/exercises/two-independent-poisson-processes]].

### 2021-06-22, AY 2020/2021, E1

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 1$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(1)=1 \mid X_1(2)+X_2(2)=4]$ and $P[X_1(2)+X_2(2)=4 \mid X_1(1)=1]$.
>
> (b) Compute $P[X_1(1)+X_2(1)=2 \mid X_1(2)=0]$ and $P[X_1(1)+X_2(1)=2 \mid X_1(2)=1]$.

### 2022-06-24, AY 2021/2022, E1

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 1$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(1)=1 \mid X_1(1)+X_2(1)=2]$ and $P[X_1(1)+X_2(1)=2 \mid X_1(1)=1]$.
>
> (b) Compute $P[X_1(1)=1 \mid X_1(2)+X_2(2)=4]$ and $P[X_1(2)+X_2(2)=4 \mid X_1(1)=1]$.

### 2023-06-16, AY 2021/2022 as printed, E1

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 1$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(1)=1 \mid X_1(1)+X_2(1)=2]$ and $P[X_1(1)+X_2(1)=2 \mid X_1(1)=1]$.
>
> (b) Compute $P[X_1(1)=1 \mid X_1(2)+X_2(2)=4]$ and $P[X_1(2)+X_2(2)=4 \mid X_1(1)=1]$.

### 2023-07-03, AY 2022/2023, E3

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 0.5$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(1)=1 \mid X_1(1)+X_2(1)=3]$ and $P[X_1(1)+X_2(1)=3 \mid X_1(1)=1]$.
>
> (b) Compute $P[X_2(1)=1 \mid X_1(2)+X_2(2)=3]$ and $P[X_1(2)+X_2(2)=3 \mid X_2(1)=1]$.

### 2024-02-23, AY 2022/2023, E3

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 0.5$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(1)=1 \mid X_1(1)+X_2(1)=3]$ and $P[X_1(1)+X_2(1)=3 \mid X_1(1)=1]$.
>
> (b) Compute $P[X_2(1)=1 \mid X_1(2)+X_2(2)=3]$ and $P[X_1(2)+X_2(2)=3 \mid X_2(1)=1]$.

### 2024-06-12, AY 2023/2024, E1

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 0.5$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(2)=1 \mid X_1(3)=2]$ and $P[X_1(3)=2 \mid X_1(2)=1]$.
>
> (b) Compute $P[X_2(1)=1 \mid X_1(2)+X_2(2)=3]$ and $P[X_1(2)+X_2(2)=3 \mid X_2(1)=1]$.

### 2024-07-01, ICT, AY 2023/2024, E1

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 0.5$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_1(2)=1 \mid X_1(3)=2]$ and $P[X_1(3)=2 \mid X_1(2)=1]$.
>
> (b) Compute $P[X_2(1)=1 \mid X_1(2)+X_2(2)=3]$ and $P[X_1(2)+X_2(2)=3 \mid X_2(1)=1]$.

### 2024-07-01, Cybersecurity, AY 2023/2024, E4

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 1$ and $\lambda_2 = 2$, respectively.
>
> (a) Compute $P[X_1(2)=1 \mid X_1(3)=2]$ and $P[X_1(3)=2 \mid X_1(2)=1]$.
>
> (b) Compute $P[X_2(1)=1 \mid X_1(2)+X_2(2)=3]$ and $P[X_1(2)+X_2(2)=3 \mid X_2(1)=1]$.

### 2024-07-15, Cybersecurity, AY 2023/2024, E1

Frequency: 9.

> Consider two independent Poisson processes $X_1(t)$ and $X_2(t)$, where $X_i(t)$ is the number of arrivals for process $i$ during $[0,t]$. The average number of arrivals per unit time of the two processes is $\lambda_1 = 0.5$ and $\lambda_2 = 1$, respectively.
>
> (a) Compute $P[X_2(2)=1 \mid X_1(2)+X_2(2)=2]$ and $P[X_1(2)+X_2(2)=2 \mid X_2(2)=1]$.
>
> (b) Compute $P[X_2(1)=1 \mid X_1(2)+X_2(2)=3]$ and $P[X_1(2)+X_2(2)=3 \mid X_2(1)=1]$.

## Finite Markov-Chain Matrix Analysis

Overall frequency: 10.

Related pages: [[wiki/concepts/markov-chain]], [[wiki/concepts/communicating-classes]], [[wiki/concepts/recurrence]], [[wiki/concepts/stationary-distribution]], [[wiki/theorems/basic-limit-theorem]], [[wiki/theorems/transient-to-recurrent-limit]].

## Five-State Classification, Absorption, Limits, and First Passage

Frequency: 7.

### 2021-06-22, AY 2020/2021, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 0 & 1 & 0\\
> 0 & 0.4 & 0 & 0 & 0.6\\
> 0 & 0 & 0.5 & 0.2 & 0.3\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.3 & 0 & 0 & 0.7
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 4.

### 2022-06-24, AY 2021/2022, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 0 & 1 & 0\\
> 0 & 0.7 & 0 & 0 & 0.3\\
> 0 & 0 & 0.4 & 0.2 & 0.4\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.6 & 0 & 0 & 0.4
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 4.

### 2023-06-16, AY 2021/2022 as printed, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 0 & 1 & 0\\
> 0 & 0.7 & 0 & 0 & 0.3\\
> 0 & 0 & 0.4 & 0.2 & 0.4\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.6 & 0 & 0 & 0.4
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 4.

### 2024-06-12, AY 2023/2024, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 1 & 0 & 0\\
> 0 & 0.6 & 0 & 0.4 & 0\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.2 & 0 & 0.8 & 0\\
> 0 & 0 & 0.2 & 0.1 & 0.7
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 1.

### 2024-07-01, ICT, AY 2023/2024, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 1 & 0 & 0\\
> 0 & 0.6 & 0 & 0.4 & 0\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.2 & 0 & 0.8 & 0\\
> 0 & 0 & 0.2 & 0.1 & 0.7
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 1.

### 2024-07-01, Cybersecurity, AY 2023/2024, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 1 & 0 & 0\\
> 0 & 0.4 & 0 & 0.6 & 0\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.2 & 0 & 0.8 & 0\\
> 0 & 0 & 0.2 & 0.1 & 0.7
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 0.

### 2024-07-15, Cybersecurity, AY 2023/2024, E3

Frequency: 7.

> Consider a Markov chain with the following transition matrix (states are numbered from 0 to 4):
>
> $$
> P =
> \begin{pmatrix}
> 0 & 0 & 1 & 0 & 0\\
> 0 & 0.6 & 0 & 0.4 & 0\\
> 1 & 0 & 0 & 0 & 0\\
> 0 & 0.2 & 0 & 0.8 & 0\\
> 0 & 0 & 0.2 & 0.1 & 0.7
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, identify the classes, classify the states, and compute the probabilities of absorption in all recurrent classes starting from each transient state.
>
> (b) Compute $\lim_{n\to\infty} P^n$ and $\lim_{n\to\infty} \frac{1}{n}\sum_{k=0}^{n-1} P^k$.
>
> (c) Compute the average recurrence time for all states, and the average first passage time from any state to state 3.

## Three-State Absorbing-Chain Evolution and Expected Visits

Frequency: 3.

### 2021-07-13, AY 2020/2021, E2

Frequency: 3.

> Consider a Markov chain $X_n$ with the following transition matrix (states are numbered from 0 to 2):
>
> $$
> P =
> \begin{pmatrix}
> 0.3 & 0.5 & 0.2\\
> 0.5 & 0.3 & 0.2\\
> 0 & 0 & 1
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, and find the probability distribution of $X_1$, $X_2$, and $X_{1000}$, given $X_0=0$.
>
> (b) Let $W_{ij}^{(n)} = E[\sum_{k=0}^{n-1} I\{X_k=j\}\mid X_0=i]$ be the average number of visits to state $j$ during the first $n$ time slots, given that the chain starts in state $i$. Compute $\lim_{n\to\infty} W_{0j}^{(n)}$ for $j=0,1,2$.
>
> (c) Compute the average duration of the transient evolution of the chain, i.e., the time index at which the chain is absorbed.

### 2023-07-03, AY 2022/2023, E2

Frequency: 3.

> Consider a Markov chain $X_n$ with the following transition matrix (states are numbered from 0 to 2):
>
> $$
> P =
> \begin{pmatrix}
> 0.2 & 0.4 & 0.4\\
> 0.4 & 0.2 & 0.4\\
> 0 & 0 & 1
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, and find the probability distribution of $X_1$, $X_2$, and $X_{1000}$, given $X_0=0$.
>
> (b) Let $W_{ij}^{(n)} = E[\sum_{k=0}^{n-1} I\{X_k=j\}\mid X_0=i]$ be the average number of visits to state $j$ during the first $n$ time slots, given that the chain starts in state $i$. Compute $\lim_{n\to\infty} W_{0j}^{(n)}$ for $j=0,1,2$.
>
> (c) Compute the average duration of the transient evolution of the chain, i.e., the time index at which the chain is absorbed, given $X_0=i$ for $i=0,1$.

### 2024-02-23, AY 2022/2023, E2

Frequency: 3.

> Consider a Markov chain $X_n$ with the following transition matrix (states are numbered from 0 to 2):
>
> $$
> P =
> \begin{pmatrix}
> 0.2 & 0.4 & 0.4\\
> 0.4 & 0.2 & 0.4\\
> 0 & 0 & 1
> \end{pmatrix}.
> $$
>
> (a) Draw the transition diagram, and find the probability distribution of $X_1$, $X_2$, and $X_{1000}$, given $X_0=0$.
>
> (b) Let $W_{ij}^{(n)} = E[\sum_{k=0}^{n-1} I\{X_k=j\}\mid X_0=i]$ be the average number of visits to state $j$ during the first $n$ time slots, given that the chain starts in state $i$. Compute $\lim_{n\to\infty} W_{0j}^{(n)}$ for $j=0,1,2$.
>
> (c) Compute the average duration of the transient evolution of the chain, i.e., the time index at which the chain is absorbed, given $X_0=i$ for $i=0,1$.

## Renewal/Reward Availability Applications

Overall frequency: 10.

Related pages: [[wiki/concepts/renewal-process]], [[wiki/concepts/renewal-reward-process]], [[wiki/theorems/renewal-reward-theorem]], [[wiki/concepts/poisson-process]].

## Single-Node Cleanup and Manual-Restore Model

Frequency: 5.

### 2021-07-13, AY 2020/2021, E3

Frequency: 5.

> Consider a network node able to handle traffic at 10 Gbps under normal conditions. The node is subject to attacks, that arrive according to a Poisson process of rate $\lambda = 1/T_0$. For each attack, the node has a probability $1-\alpha$ of being infected, whereas with probability $\alpha$ the attack has no consequence. When a node gets infected, it automatically starts a clean-up process that lasts $T_1$ and occupies 70% of its resources, so that during this phase the node can only handle 3 Gbps. The clean-up process is successful with probability $\beta$ (in which case the node starts working normally), whereas with probability $1-\beta$ it fails and the node needs to be restored manually by a human operator, which takes $T_2$, during which time the node does not handle any traffic. After being manually restored, the node starts working normally.
>
> (a) By identifying an appropriate renewal cycle, compute the fraction of the time the node is not handling any traffic and the average traffic per unit time (in Gbps) handled by the node.
>
> (b) Compute how often (e.g., how many times a day on average) a human operator's intervention is needed.
>
> For all the above quantities, find mathematical expressions as a function of the parameters, and then compute their numerical values for $T_0 = 20$ minutes, $T_1 = 20$ minutes, $T_2 = 3$ hours, $\alpha = 0.98$, $\beta = 0.9$.

### 2023-07-03, AY 2022/2023, E4

Frequency: 5.

> Consider a network node able to handle traffic at 20 Gbps under normal conditions. The node is subject to attacks, that arrive according to a Poisson process of rate $\lambda = 1/T_0$. For each attack, the node has a probability $1-\alpha$ of being infected, whereas with probability $\alpha$ the attack has no consequence. When a node gets infected, it automatically starts a clean-up process that lasts $T_1$ and occupies 50% of its resources, so that during this phase the node can only handle 10 Gbps. The clean-up process is successful with probability $\beta$ (in which case the node starts working normally), whereas with probability $1-\beta$ it fails and the node needs to be restored manually by a human operator, which takes $T_2$, during which time the node does not handle any traffic. After being manually restored, the node starts working normally.
>
> (a) By identifying an appropriate renewal cycle, compute the fraction of the time the node is not handling any traffic.
>
> (b) Compute the average traffic per unit time (in Gbps) handled by the node.
>
> (c) Compute how often (e.g., how many times a day on average) a human operator's intervention is needed.
>
> For all the above quantities, find mathematical expressions as a function of the parameters, and then compute their numerical values for $T_0 = 10$ minutes, $T_1 = 10$ minutes, $T_2 = 3$ hours, $\alpha = 0.99$, $\beta = 0.9$.

### 2024-02-23, AY 2022/2023, E4

Frequency: 5.

> Consider a network node able to handle traffic at 20 Gbps under normal conditions. The node is subject to attacks, that arrive according to a Poisson process of rate $\lambda = 1/T_0$. For each attack, the node has a probability $1-\alpha$ of being infected, whereas with probability $\alpha$ the attack has no consequence. When a node gets infected, it automatically starts a clean-up process that lasts $T_1$ and occupies 50% of its resources, so that during this phase the node can only handle 10 Gbps. The clean-up process is successful with probability $\beta$ (in which case the node starts working normally), whereas with probability $1-\beta$ it fails and the node needs to be restored manually by a human operator, which takes $T_2$, during which time the node does not handle any traffic. After being manually restored, the node starts working normally.
>
> (a) By identifying an appropriate renewal cycle, compute the fraction of the time the node is not handling any traffic.
>
> (b) Compute the average traffic per unit time (in Gbps) handled by the node.
>
> (c) Compute how often (e.g., how many times a day on average) a human operator's intervention is needed.
>
> For all the above quantities, find mathematical expressions as a function of the parameters, and then compute their numerical values for $T_0 = 10$ minutes, $T_1 = 10$ minutes, $T_2 = 3$ hours, $\alpha = 0.99$, $\beta = 0.9$.

### 2024-07-01, ICT, AY 2023/2024, E4

Frequency: 5.

> Consider a network node able to handle traffic at 10 Gbps under normal conditions. The node is subject to attacks, that arrive according to a Poisson process of rate $\lambda = 1/T_1$. For each attack, the node has a probability $\alpha$ of being infected, whereas with probability $1-\alpha$ the attack has no consequence. When a node gets infected, it automatically starts a clean-up process that lasts $T_2$ and occupies 50% of its resources, so that during this phase the node can only handle 5 Gbps. The clean-up process is successful with probability $1-\beta$ (in which case the node starts working normally), whereas with probability $\beta$ it fails and the node needs to be restored manually by a human operator, which takes $T_3$, during which time the node does not handle any traffic. After being manually restored, the node starts working normally.
>
> (a) By identifying an appropriate renewal cycle, compute the fraction of the time the node is not handling any traffic and the average traffic per unit time (in Gbps) handled by the node.
>
> (b) Compute how often (e.g., how many times a day on average) a human operator's intervention is needed.
>
> For all the above quantities, find mathematical expressions as a function of the parameters, and then compute their numerical values for $T_1 = 10$ minutes, $T_2 = 10$ minutes, $T_3 = 3$ hours, $\alpha = 0.02$, $\beta = 0.1$.

### 2024-07-01, Cybersecurity, AY 2023/2024, E2

Frequency: 5.

> Consider a network node able to handle traffic at 20 Gbps under normal conditions. The node is subject to attacks, that arrive according to a Poisson process of rate $\lambda = 1/T_1$. For each attack, the node has a probability $\beta$ of being infected, whereas with probability $1-\beta$ the attack has no consequence. When a node gets infected, it automatically starts a clean-up process that lasts $T_2$ and occupies 70% of its resources, so that during this phase the node can only handle 6 Gbps. The clean-up process is successful with probability $1-\alpha$ (in which case the node starts working normally), whereas with probability $\alpha$ it fails and the node needs to be restored manually by a human operator, which takes $T_3$, during which time the node does not handle any traffic. After being manually restored, the node starts working normally.
>
> (a) By identifying an appropriate renewal cycle, compute the fraction of the time the node is not handling any traffic and the average traffic per unit time (in Gbps) handled by the node.
>
> (b) Compute how often (e.g., how many times a day on average) a human operator's intervention is needed.
>
> For all the above quantities, find mathematical expressions as a function of the parameters, and then compute their numerical values for $T_1 = 10$ minutes, $T_2 = 30$ minutes, $T_3 = 3$ hours, $\alpha = 0.1$, $\beta = 0.01$.

## Two-Server Attacked Streaming Node

Frequency: 5.

### 2021-06-22, AY 2020/2021, E4

Frequency: 5.

> Consider a node that contains two identical and independent servers, each able to stream data at 1 Gbps. Each server is subject to attacks according to a Poisson process with rate $\lambda = 10$ attacks/hour, and each attack is effective with probability $1/9$, whereas it has no consequences with probability $8/9$ (Hint: only consider the process of effective attacks). As a result of each effective attack, the server will remain inoperational (i.e., with zero streaming rate) for an exponential time with average $T = 6$ minutes, during which any arriving attack will have no effect, and then will resume normal operations.
>
> (a) Compute the fraction of time during which the node does not stream any data (i.e., both servers are inoperational), and the average duration of a period of time during which no data is streamed.
>
> (b) By considering an appropriate renewal cycle, compute the average duration of the time interval during which the node is able to stream data without interruptions (i.e., there is always at least one server working).
>
> (c) Compute the average total streaming rate of the node in Gbps.

### 2022-06-24, AY 2021/2022, E4

Frequency: 5.

> Consider a node that contains two identical and independent servers, each able to stream data at 1 Gbps. Each server is subject to attacks according to a Poisson process with rate $\lambda = 20$ attacks/hour, and each attack is effective with probability $1/18$, whereas it has no consequences with probability $17/18$ (Hint: only consider the process of effective attacks). As a result of each effective attack, the server will remain inoperational (i.e., with zero streaming rate) for an exponential time with average $T = 6$ minutes, during which any arriving attack will have no effect, and then will resume normal operations.
>
> (a) Compute the fraction of time during which the node does not stream any data (i.e., both servers are inoperational), and the average duration of a period of time during which no data is streamed.
>
> (b) By considering an appropriate renewal cycle, compute the average duration of the time interval during which the node is able to stream data without interruptions (i.e., there is always at least one server working).
>
> (c) Compute the average total streaming rate of the node in Gbps.

### 2023-06-16, AY 2021/2022 as printed, E4

Frequency: 5.

> Consider a node that contains two identical and independent servers, each able to stream data at 1 Gbps. Each server is subject to attacks according to a Poisson process with rate $\lambda = 20$ attacks/hour, and each attack is effective with probability $1/18$, whereas it has no consequences with probability $17/18$ (Hint: only consider the process of effective attacks). As a result of each effective attack, the server will remain inoperational (i.e., with zero streaming rate) for an exponential time with average $T = 6$ minutes, during which any arriving attack will have no effect, and then will resume normal operations.
>
> (a) Compute the fraction of time during which the node does not stream any data (i.e., both servers are inoperational), and the average duration of a period of time during which no data is streamed.
>
> (b) By considering an appropriate renewal cycle, compute the average duration of the time interval during which the node is able to stream data without interruptions (i.e., there is always at least one server working).
>
> (c) Compute the average total streaming rate of the node in Gbps.

### 2024-06-12, AY 2023/2024, E4

Frequency: 5.

> Consider a node that contains two identical and independent servers, each able to stream data at 2.5 Gbps. Each server is subject to attacks according to a Poisson process with rate $\lambda = 20$ attacks/hour, and each attack is effective with probability $1/9$, whereas it has no consequences with probability $8/9$ (Hint: only consider the process of effective attacks). As a result of each effective attack, the server will remain inoperational (i.e., with zero streaming rate) for an exponential time with average $T = 3$ minutes, during which any arriving attack will have no effect, and then will resume normal operations.
>
> (a) Compute the fraction of time during which the node does not stream any data (i.e., both servers are inoperational), and the average duration of a period of time during which no data is streamed.
>
> (b) By considering an appropriate renewal cycle, compute the average duration of the time interval during which the node is able to stream data without interruptions (i.e., there is always at least one server working).
>
> (c) Compute the average total streaming rate of the node in Gbps.

### 2024-07-15, Cybersecurity, AY 2023/2024, E4

Frequency: 5.

> Consider a node that contains two identical and independent servers, each able to stream data at rate $R$. Each server is subject to attacks according to a Poisson process with rate $\lambda$, and each attack is effective with probability $\alpha$, whereas it has no consequences with probability $1-\alpha$ (Hint: only consider the process of effective attacks). As a result of each effective attack, the server will remain inoperational (i.e., with zero streaming rate) for an exponential time with average $T$, during which any arriving attack will have no effect, and then will resume normal operations.
>
> (a) Compute the fraction of time during which the node does not stream any data (i.e., both servers are inoperational), and the average duration of a period of time during which no data is streamed.
>
> (b) By considering an appropriate renewal cycle, compute the average duration of the time interval during which the node is able to stream data without interruptions (i.e., there is always at least one server working).
>
> (c) Compute the average total streaming rate of the node in Gbps.
>
> For all the above quantities, find mathematical expressions as a function of the parameters, and then compute their numerical values for $R = 2.5$ Gbps, $\lambda = 20$ attacks/hour, $\alpha = 1/9$, and $T = 3$ minutes.

## Proof and Theorem Prompts

## Renewal-Process Limit for $N(t)/t$

Frequency: 4 official occurrences; 5 if the 2024-07-01 Cybersecurity handwritten solution pages are counted as an inferred occurrence.

Related pages: [[wiki/concepts/renewal-process]], [[wiki/theorems/elementary-renewal-theorem]].

### 2021-06-22, AY 2020/2021, T3

Frequency: 4 official.

> For a renewal process, state precisely (also providing a formal proof) what is the value of
>
> $$
> \lim_{t\to\infty} \frac{N(t)}{t}.
> $$

### 2022-06-24, AY 2021/2022, T3

Frequency: 4 official.

> For a renewal process, state precisely (also providing a formal proof) what is the value of
>
> $$
> \lim_{t\to\infty} \frac{N(t)}{t}.
> $$

### 2024-02-23, AY 2022/2023, T1

Frequency: 4 official.

> For a renewal process, state precisely (also providing a formal proof) what is the value of
>
> $$
> \lim_{t\to\infty} \frac{N(t)}{t}.
> $$

### 2024-07-01, ICT, AY 2023/2024, T3

Frequency: 4 official.

> For a renewal process, state precisely (also providing a formal proof) what is the value of
>
> $$
> \lim_{t\to\infty} \frac{N(t)}{t}.
> $$

### 2024-07-01, Cybersecurity, AY 2023/2024, T3 inferred from handwritten solution pages

Frequency: 5 if inferred occurrences are counted.

> Inferred prompt: for a renewal process, state precisely and prove the value of
>
> $$
> \lim_{t\to\infty} \frac{N(t)}{t}.
> $$

## Recurrence Preserved across Communicating States

Frequency: 3 official occurrences; 4 if the 2024-07-01 Cybersecurity handwritten solution pages are counted as an inferred occurrence.

Related pages: [[wiki/concepts/recurrence]], [[wiki/concepts/communicating-classes]], [[wiki/theorems/recurrence-criterion]].

### 2021-06-22, AY 2020/2021, T1

Frequency: 3 official.

> Prove that if states $i$ and $j$ of a Markov chain communicate and $i$ is recurrent, then $j$ is also recurrent.

### 2022-06-24, AY 2021/2022, T1

Frequency: 3 official.

> Prove that if states $i$ and $j$ of a Markov chain communicate and $i$ is recurrent, then $j$ is also recurrent (if in the proof you use a previous result, state it precisely without proof).

### 2024-07-01, ICT, AY 2023/2024, T1

Frequency: 3 official.

> Prove that if states $i$ and $j$ of a Markov chain communicate and $i$ is recurrent, then $j$ is also recurrent.

### 2024-07-01, Cybersecurity, AY 2023/2024, T1 inferred from handwritten solution pages

Frequency: 4 if inferred occurrences are counted.

> Inferred prompt: prove that if states $i$ and $j$ of a Markov chain communicate and $i$ is recurrent, then $j$ is also recurrent.

## Poisson Interarrival Times Are iid Exponential

Frequency: 3 official occurrences; 4 if the 2024-07-01 Cybersecurity handwritten solution pages are counted as an inferred occurrence.

Related pages: [[wiki/concepts/poisson-process]], [[wiki/concepts/exponential-distribution]], [[wiki/theorems/poisson-interarrival-exponential]].

### 2021-07-13, AY 2020/2021, T1

Frequency: 3 official.

> For a Poisson process of rate $\lambda$, prove that the interarrival times are iid exponential with mean $1/\lambda$.

### 2024-02-23, AY 2022/2023, T2

Frequency: 3 official.

> For a Poisson process of rate $\lambda$, prove that the interarrival times are iid exponential with mean $1/\lambda$.

### 2024-07-01, ICT, AY 2023/2024, T2

Frequency: 3 official.

> For a Poisson process of rate $\lambda$, prove that the interarrival times are iid exponential with mean $1/\lambda$.

### 2024-07-01, Cybersecurity, AY 2023/2024, T2 inferred from handwritten solution pages

Frequency: 4 if inferred occurrences are counted.

> Inferred prompt: for a Poisson process of rate $\lambda$, prove that the interarrival times are iid exponential with mean $1/\lambda$.

## Conditional Distribution of Poisson Counts Given a Total Count

Frequency: 2.

Related pages: [[wiki/concepts/poisson-process]], [[wiki/theorems/binomial-conditional-distribution]], [[wiki/theorems/conditional-arrival-times-uniform]].

### 2021-06-22, AY 2020/2021, T2

Frequency: 2.

> For a Poisson process $X(t)$ of rate $\lambda$, state and derive the expression of $P[X(u)=k \mid X(t)=n]$ for the two cases (i) $0<u<t$, $0\leq k\leq n$ and (ii) $0<t<u$, $0\leq n\leq k$.

### 2022-06-24, AY 2021/2022, T2

Frequency: 2.

> For a Poisson process $X(t)$ of rate $\lambda$, state and derive the expression of $P[X(u)=k \mid X(t)=n]$ for the two cases (i) $0<u<t$, $0\leq k\leq n$ and (ii) $0<t<u$, $0\leq n\leq k$.

## One-Off Proof Prompts Observed

These appeared once in the official Part B pages and are not part of the high-frequency list:

- 2021-07-13, T2: prove that period is a class property for Markov chains.
- 2021-07-13, T3: derive an expression for $E[S_{N(t)+1}]$ for a renewal process.
- 2024-02-23, T3: prove that a Markov chain with a finite number of states must have at least one positive recurrent state.
