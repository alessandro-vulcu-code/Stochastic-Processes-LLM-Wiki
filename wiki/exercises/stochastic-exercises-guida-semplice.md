---
type: exercise
tags: [exercise, exam-prep, markov-chains, poisson-process, renewal-process, gobackn-protocol, queueing]
sources: [stochastic-exercises-guida-semplice, lecture-notes-ch2, lecture-notes-ch3, lecture-notes-ch4, lecture-notes-ch5, lecture-notes-ch6]
related: [gobackn-protocol, renewal-reward-process, m-g-infinity-queue, absorbing-markov-chain, conditional-probability]
---

# Stochastic Exercises Guida Semplice - Exam Method Sheet

This page distills `raw/Stochastic_exercises_guida_semplice.pdf` into reusable exam templates. The source is mostly handwritten, so the wiki version keeps the stable methods and links each one to the formal result that justifies it.

## GoBackN over a Two-State Markov Channel

Use states $0=\text{good}$ and $1=\text{bad}$ unless the exercise says otherwise. If the channel matrix is

$$
C=\begin{pmatrix}
p_{00} & p_{01}\\
p_{10} & p_{11}
\end{pmatrix},
$$

start by solving

$$
\pi=\pi C,\qquad \pi_0+\pi_1=1.
$$

Without retransmission, throughput equals the stationary probability of a good slot:

$$
\eta_{\text{direct}}=\pi_0.
$$

For GoBackN with round-trip delay $m$ and error-free feedback, compute $C^m$. The practical formula used in the guide is

$$
\eta=\frac{p_{10}^{(m)}}{p_{10}^{(m)}+m p_{01}}.
$$

For iid packet errors with probability $\epsilon$,

$$
\eta_{iid}=\frac{1-\epsilon}{1-\epsilon+m\epsilon}.
$$

For iid feedback error probability $\delta$, use the feedback-error version in [[wiki/theorems/gobackn-throughput-markov-errors|GoBackN Throughput with Markov Errors]]:

$$
\eta=
\frac{(1-\delta)p_{10}^{(m)}}
{(1-\delta+m\delta)p_{10}^{(m)}+
m[(1-\delta)p_{01}+\delta p_{01}^{(m)}]}.
$$

References: [[wiki/concepts/gobackn-protocol|GoBackN Protocol]], [[wiki/concepts/renewal-reward-process|Renewal Reward Process]].

## Renewal Cycle with One Server

For attack/recovery models, identify one full cycle from "normal" back to "normal." In the source's one-server template:

- attacks arrive as a Poisson process with mean inter-attack time $T_0$;
- each attack infects the node with probability $1-\alpha$;
- cleanup lasts $T_1$ and succeeds with probability $\beta$;
- failed cleanup triggers manual repair lasting $T_2$.

The number of attacks until infection is geometric with mean $1/(1-\alpha)$, so the mean normal time before infection is

$$
T_N=\frac{T_0}{1-\alpha}.
$$

The mean cycle length is

$$
E[C]=\frac{T_0}{1-\alpha}+T_1+T_2(1-\beta).
$$

If manual repair is the only no-traffic state, then

$$
P(\text{no traffic})
=
\frac{T_2(1-\beta)}
{\frac{T_0}{1-\alpha}+T_1+T_2(1-\beta)}.
$$

If normal traffic rate is $10$ Gbps and cleanup traffic rate is $3$ Gbps, then

$$
\text{average traffic}
=
\frac{10\frac{T_0}{1-\alpha}+3T_1}
{\frac{T_0}{1-\alpha}+T_1+T_2(1-\beta)}.
$$

Interventions per day:

$$
\frac{1440}{E[C]}(1-\beta)
$$

when times are measured in minutes. Average days between interventions is the reciprocal. Reference: [[wiki/theorems/renewal-reward-theorem|Renewal Reward Theorem]].

## Renewal Cycle with Two Independent Servers

For two identical independent servers, analyze one server first, then combine probabilities.

If effective attacks arrive at rate $\lambda_e$ and each down period has mean $T$, then one server has

$$
P(\text{down})=\frac{T}{1/\lambda_e+T}.
$$

For independent servers,

$$
P(\text{both down})=P(\text{down})^2.
$$

In the source example, $\lambda=10$ attacks/hour, effective probability $1/9$, and $T=6$ minutes. Thus $\lambda_e=1/6$ per minute, the mean up time is $54$ minutes, and

$$
P(\text{one server down})=\frac{6}{54+6}=\frac{1}{10},
\qquad
P(\text{both down})=\frac{1}{100}.
$$

When both repair times are exponential with mean $6$ minutes, the mean time until at least one server returns is half the mean:

$$
E[\text{both-down duration}]=3\text{ minutes}.
$$

Using

$$
P(\text{both down})=\frac{E[\text{both-down duration}]}{E[\text{cycle}]},
$$

the cycle mean is $300$ minutes, and the mean uninterrupted interval with at least one server working is

$$
300\left(1-\frac{1}{100}\right)=297\text{ minutes}.
$$

For two $1$ Gbps servers, average streaming rate is

$$
2P(\text{both up})+1P(\text{exactly one up})
=2(0.9)^2+2(0.9)(0.1)=1.8\text{ Gbps}.
$$

## M/G/infinity Active-Population Counts

For Poisson arrivals with rate $\lambda$ and service/lifetime CDF $G$, the number $X(t)$ still active at time $t$ is Poisson with mean

$$
\lambda_{pt}=\lambda\int_0^t [1-G(y)]\,dy.
$$

Thus

$$
E[X(t)]=\lambda_{pt},
\qquad
P(X(t)=m)=e^{-\lambda_{pt}}\frac{\lambda_{pt}^m}{m!}.
$$

For exponential service with mean $6$ minutes and $\lambda=100/60=5/3$ calls/minute,

$$
1-G(y)=e^{-y/6},
\qquad
\lambda_{pt}=10(1-e^{-t/6}).
$$

For uniform service on $[2,10]$ minutes,

$$
1-G(y)=
\begin{cases}
1, & 0\le y<2,\\
\frac{10-y}{8}, & 2\le y\le 10,\\
0, & y>10.
\end{cases}
$$

Split the integral at $2$ and $10$ when computing $\lambda_{pt}$. Reference: [[wiki/concepts/m-g-infinity-queue|M/G/infinity Queue]].

## Finite Markov-Chain Distributions

If $X_0=i$, use the row vector $e_i$:

$$
\mathcal{L}(X_n)=e_iP^n.
$$

For large $n$, do not blindly replace $e_iP^n$ by a stationary distribution. First classify the chain:

- finite irreducible aperiodic class: $P^n$ converges to the stationary law;
- periodic closed class: ordinary $P^n$ may oscillate;
- reducible chain: transient states feed recurrent classes with absorption probabilities.

Reference: [[wiki/concepts/limiting-probability-distribution|Limiting Probability Distribution]].

### Absorbing Three-State Example

The source includes the absorbing chain

$$
P=
\begin{pmatrix}
0.3 & 0.5 & 0.2\\
0.5 & 0.3 & 0.2\\
0 & 0 & 1
\end{pmatrix},
\qquad X_0=0.
$$

Then

$$
X_1=(0.3,0.5,0.2),
$$

and

$$
X_2=(0.34,0.30,0.36).
$$

State $2$ is absorbing, and states $0,1$ are transient. Therefore

$$
X_{1000}\approx(0,0,1),
$$

with convergence to $(0,0,1)$ as $n\to\infty$.

For expected visits to transient states, use

$$
Q=
\begin{pmatrix}
0.3 & 0.5\\
0.5 & 0.3
\end{pmatrix},
\qquad
N=(I-Q)^{-1}
=
\begin{pmatrix}
35/12 & 25/12\\
25/12 & 35/12
\end{pmatrix}.
$$

Starting from $0$,

$$
\lim_{n\to\infty}W_{00}^{(n)}=\frac{35}{12},
\qquad
\lim_{n\to\infty}W_{01}^{(n)}=\frac{25}{12}.
$$

For the absorbing state,

$$
\lim_{n\to\infty}W_{02}^{(n)}=\infty,
$$

because after absorption the chain remains in state $2$ and visits keep being counted.

Mean absorption time is the row sum of $N$:

$$
E_0[T_{\{2\}}]=\frac{35}{12}+\frac{25}{12}=5.
$$

References: [[wiki/concepts/absorbing-markov-chain|Absorbing Markov Chain]], [[wiki/concepts/fundamental-matrix|Fundamental Matrix]], [[wiki/theorems/mean-absorption-time|Mean Absorption Time via Fundamental Matrix]].

## Reducible Markov Chains with Recurrent Classes

Workflow:

1. Draw the transition diagram.
2. Identify closed recurrent classes and transient states.
3. Compute absorption probabilities from each transient state into each closed class.
4. For each closed aperiodic class, solve the class stationary distribution.
5. For periodic classes, ordinary $P^n$ may fail to converge, but the Cesaro average
   $$
   \frac1n\sum_{k=0}^{n-1}P^k
   $$
   uses the class stationary distribution.

Mean recurrence time for positive recurrent state $i$:

$$
m_i=\frac{1}{\pi_i}.
$$

Mean first-passage times solve

$$
\theta_{ij}=1+\sum_{k\ne j}p_{ik}\theta_{kj}.
$$

If $j$ is unreachable from $i$, then $\theta_{ij}=\infty$.

References: [[wiki/concepts/state-classification|State Classification]], [[wiki/theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]], [[wiki/theorems/mean-first-passage-time|Mean First Passage Time]].

## Markov Path Conditioning

Use

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}.
$$

For fixed Markov paths, factor the numerator as a product of one-step probabilities. For example, if $X_0=0$,

$$
P(X_1=a,X_2=b,X_3=c\mid X_0=0)
=p_{0a}p_{ab}p_{bc}.
$$

If the denominator only fixes endpoints, replace the middle segment by an $n$-step transition probability, such as $p_{ij}^{(2)}=(P^2)_{ij}$.

Reference: [[wiki/theorems/markov-chain-factorization|Markov Chain Factorization]].

## Two Poisson Processes and Interval Conditioning

For independent Poisson processes $X_1,X_2$ with rates $\lambda_1,\lambda_2$, same-interval conditioning gives binomial splitting:

$$
P(X_1(t)=k\mid X_1(t)+X_2(t)=m)
=
\binom{m}{k}
\left(\frac{\lambda_1}{\lambda_1+\lambda_2}\right)^k
\left(\frac{\lambda_2}{\lambda_1+\lambda_2}\right)^{m-k}.
$$

For one process and a subinterval $0<s<t$,

$$
P(X(s)=k\mid X(t)=m)
=
\binom{m}{k}
\left(\frac{s}{t}\right)^k
\left(1-\frac{s}{t}\right)^{m-k}.
$$

If the conditioning gives information about the past and asks about a future increment, separate the already-known contribution and use independent increments for the remaining future contribution. If conditioning says a required past count is impossible, reduce that case to probability zero before calculating.

References: [[wiki/theorems/binomial-conditional-distribution|Binomial Conditional Distribution]], [[wiki/theorems/two-processes-conditional-distribution|Conditional Distribution for Two Concurrent Poisson Processes]], [[wiki/concepts/poisson-process|Poisson Process]].

## Sources

- [[wiki/sources/stochastic-exercises-guida-semplice]] - visual source for these exam templates.
- [[wiki/sources/lecture-notes-ch2]] - Markov-chain foundations.
- [[wiki/sources/lecture-notes-ch3]] - long-run Markov-chain classification.
- [[wiki/sources/lecture-notes-ch4]] - Poisson-process and M/G/infinity formulas.
- [[wiki/sources/lecture-notes-ch5]] - renewal reward and regenerative cycles.
- [[wiki/sources/lecture-notes-ch6]] - GoBackN throughput theory.
