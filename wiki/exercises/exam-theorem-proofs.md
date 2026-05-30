---
type: exercise
tags: [exercise, exam-prep, markov-chains, poisson-process, renewal-process]
sources: [exams-theorems, lecture-notes-ch3, lecture-notes-ch4, lecture-notes-ch5]
related: [[theorems/finite-state-positive-recurrence]],[[theorems/chapman-kolmogorov]], [[theorems/elementary-renewal-theorem]], [[theorems/period-class-property]], [[theorems/binomial-conditional-distribution]], [[theorems/poisson-interarrival-exponential]]
---

# Exam Theorem Proofs

These notes answer the twelve prompts in [[sources/exams-theorems|Exams Theorems]]. Renewal-process notation: $X_1,X_2,\ldots$ are positive i.i.d. interarrival times, $\mu=\mathbb{E}[X_1]$, $S_n=X_1+\cdots+X_n$, $S_0=0$, $N(t)=\max\{n:S_n\leq t\}$, and $M(t)=\mathbb{E}[N(t)]$.

## 1. Finite Markov Chains Have No Null Recurrent States

**Theorem.** A Markov chain with a finite state space cannot contain a null recurrent state.

**Proof.** Suppose $i$ is recurrent and let $C$ be its communicating class. First, $C$ is closed. Indeed, if some $j\notin C$ were reachable from $i$, then after reaching $j$ the chain could not return to $i$; otherwise $j$ would communicate with $i$ and would belong to $C$. This would give a positive probability of never returning to $i$, contradicting recurrence.

Thus $C$ is a finite closed irreducible Markov chain. Fix $i\in C$. For every $x\in C$, irreducibility gives a path from $x$ to $i$ with positive probability. Since $C$ is finite, choose $L<\infty$ and $\varepsilon>0$ such that, from every $x\in C$,
$$
\mathbb{P}_x(T_i\leq L)\geq \varepsilon,
$$
where $T_i=\inf\{n\geq 0:X_n=i\}$.

By the Markov property,
$$
\mathbb{P}_x(T_i>rL)\leq (1-\varepsilon)^r,\qquad r\geq 0.
$$
Hence $\mathbb{E}_x[T_i]\leq L/\varepsilon<\infty$. Starting from $i$, after one step the chain is still in $C$, so the first positive return time $T_i^+=\inf\{n\geq1:X_n=i\}$ has finite expectation. Therefore $i$ is positive recurrent. Since every recurrent state in a finite chain is positive recurrent, no recurrent state can be null recurrent. $\square$

## 2. Renewal Identity for $\mathbb{E}[S_{N(t)+1}]$

**Theorem.** For a renewal process with finite mean $\mu=\mathbb{E}[X_1]$,
$$
\mathbb{E}[S_{N(t)+1}]=\mu(M(t)+1).
$$

**Proof.** Let
$$
A(t)=\mathbb{E}[S_{N(t)+1}]
$$
be the expected epoch of the first renewal strictly after $t$. Condition on $X_1=x$.

If $x>t$, no renewal has occurred before $t$, so the next renewal epoch is $x$. If $x\leq t$, the process renews at time $x$ and restarts independently; the expected additional time to the first renewal after $t$ is $A(t-x)$. Therefore
$$
\mathbb{E}[S_{N(t)+1}\mid X_1=x]
=
\begin{cases}
x, & x>t,\\
x+A(t-x), & x\leq t.
\end{cases}
$$
Integrating with respect to $F$, distribution of $X_1$, gives
$$
\begin{aligned}
A(t)
&=\int_0^t [x+A(t-x)]\,dF(x)+\int_t^\infty x\,dF(x)\\
&=\int_0^\infty x\,dF(x)+\int_0^t A(t-x)\,dF(x)\\
&=\mu+\int_0^t A(t-x)\,dF(x).
\end{aligned}
$$
This is a renewal equation with constant forcing term $\mu$. The standard solution of
$$
Z(t)=a(t)+\int_0^t Z(t-x)\,dF(x)
$$
is
$$
Z(t)=a(t)+\int_0^t a(t-x)\,dM(x).
$$
Here $a(t)=\mu$, so
$$
A(t)=\mu+\mu\int_0^t dM(x)=\mu(1+M(t)).
$$
Thus $\mathbb{E}[S_{N(t)+1}]=\mu(M(t)+1)$. $\square$

## 3. Chapman-Kolmogorov Equations

**Theorem.** For a homogeneous Markov chain,
$$
P_{ij}^{(n)}=\sum_m P_{im}^{(k)}P_{mj}^{(n-k)},\qquad k=0,1,\ldots,n.
$$

**Proof.** Starting from state $i$, decompose the event $\{X_n=j\}$ according to the intermediate state at time $k$:
$$
\begin{aligned}
P_{ij}^{(n)}
&=\mathbb{P}(X_n=j\mid X_0=i)\\
&=\sum_m \mathbb{P}(X_n=j,X_k=m\mid X_0=i)\\
&=\sum_m \mathbb{P}(X_k=m\mid X_0=i)
   \mathbb{P}(X_n=j\mid X_k=m,X_0=i).
\end{aligned}
$$
By the Markov property, conditional on $X_k=m$, the future after time $k$ is independent of the past. By homogeneity, the probability of moving from $m$ to $j$ in $n-k$ steps is $P_{mj}^{(n-k)}$. Hence
$$
P_{ij}^{(n)}=\sum_m P_{im}^{(k)}P_{mj}^{(n-k)}.
$$
For $k=0$ or $k=n$, this remains true using $P^{(0)}=I$. $\square$

## 4. Elementary Renewal Theorem

**Theorem.** If $\mu=\mathbb{E}[X_1]\in(0,\infty)$, then
$$
\lim_{t\to\infty}\frac{M(t)}{t}=\frac{1}{\mu}.
$$

**Proof.** From Theorem 2,
$$
\mathbb{E}[S_{N(t)+1}]=\mu(M(t)+1).
$$
Since $S_{N(t)+1}>t$,
$$
t<\mu(M(t)+1),
$$
so
$$
\frac{M(t)}{t}>\frac{1}{\mu}-\frac{1}{t}.
$$
Therefore
$$
\liminf_{t\to\infty}\frac{M(t)}{t}\geq \frac{1}{\mu}.
$$

For the reverse inequality, fix $a>0$ and define truncated interarrival times
$$
Y_n=\min(X_n,a),\qquad \mu_a=\mathbb{E}[Y_1].
$$
Let $N_a(t)$ and $M_a(t)$ be the renewal count and renewal function for the truncated process. Since $Y_n\leq X_n$, the truncated renewal epochs occur no later than the original ones, so
$$
N(t)\leq N_a(t),\qquad M(t)\leq M_a(t).
$$
Also $Y_n\leq a$, so the next truncated renewal after $t$ occurs no later than $t+a$:
$$
S^a_{N_a(t)+1}\leq t+a.
$$
Applying Theorem 2 to the truncated process gives
$$
\mu_a(M_a(t)+1)=\mathbb{E}[S^a_{N_a(t)+1}]\leq t+a.
$$
Thus
$$
\frac{M(t)}{t}\leq \frac{M_a(t)}{t}\leq \frac{t+a}{\mu_a t}-\frac{1}{t}.
$$
Taking $\limsup$,
$$
\limsup_{t\to\infty}\frac{M(t)}{t}\leq \frac{1}{\mu_a}.
$$
Finally let $a\to\infty$. By monotone convergence, $\mu_a\uparrow\mu$, so
$$
\limsup_{t\to\infty}\frac{M(t)}{t}\leq \frac{1}{\mu}.
$$
Combining lower and upper bounds,
$$
\lim_{t\to\infty}\frac{M(t)}{t}=\frac{1}{\mu}.
$$
$\square$

## 5. Period Is a Class Property

**Theorem.** If states $i$ and $j$ communicate, then they have the same period:
$$
i\leftrightarrow j\quad\Longrightarrow\quad d(i)=d(j).
$$

**Proof.** Let
$$
S_i=\{s\geq1:P_{ii}^{(s)}>0\}
$$
be the set of possible return times to $i$, and let $d(i)=\gcd S_i$. Since $i\leftrightarrow j$, there exist $m,n\geq1$ such that
$$
P_{ij}^{(m)}>0,\qquad P_{ji}^{(n)}>0.
$$
Take any $s\in S_i$. Then $P_{ii}^{(s)}>0$. By joining paths $j\to i$, $i\to i$, and $i\to j$,
$$
P_{jj}^{(n+s+m)}\geq P_{ji}^{(n)}P_{ii}^{(s)}P_{ij}^{(m)}>0.
$$
Thus $n+s+m\in S_j$. Repeating the $i\to i$ loop twice gives
$$
P_{jj}^{(n+2s+m)}>0,
$$
so $n+2s+m\in S_j$.

Every element of $S_j$ is divisible by $d(j)$, so
$$
n+s+m=k_1d(j),\qquad n+2s+m=k_2d(j)
$$
for integers $k_1,k_2$. Subtracting,
$$
s=(k_2-k_1)d(j).
$$
Therefore every $s\in S_i$ is divisible by $d(j)$, so $d(j)$ divides $d(i)$. Reversing the roles of $i$ and $j$ gives $d(i)$ divides $d(j)$. Hence $d(i)=d(j)$. $\square$

## 6. Conditional Poisson Count in a Subinterval

**Theorem.** Let $X(t)$ be a Poisson process of rate $\lambda$. If $0<s<t$ and $0\leq k\leq n$, then
$$
\mathbb{P}[X(s)=k\mid X(t)=n]
=
\binom{n}{k}\left(\frac{s}{t}\right)^k
\left(1-\frac{s}{t}\right)^{n-k}.
$$

**Proof.** Since $X(t)=X(s)+[X(t)-X(s)]$ and Poisson increments over disjoint intervals are independent,
$$
\begin{aligned}
\mathbb{P}[X(s)=k\mid X(t)=n]
&=\frac{\mathbb{P}[X(s)=k,\ X(t)-X(s)=n-k]}{\mathbb{P}[X(t)=n]}\\
&=\frac{
e^{-\lambda s}\frac{(\lambda s)^k}{k!}
e^{-\lambda(t-s)}\frac{(\lambda(t-s))^{n-k}}{(n-k)!}
}{
e^{-\lambda t}\frac{(\lambda t)^n}{n!}
}\\
&=\binom{n}{k}\left(\frac{s}{t}\right)^k
\left(\frac{t-s}{t}\right)^{n-k}.
\end{aligned}
$$
This is the probability mass function of a $\mathrm{Binomial}(n,s/t)$ random variable. $\square$

## 7. Recurrence Is a Class Property

**Theorem.** If states $i$ and $j$ communicate and $i$ is recurrent, then $j$ is recurrent.

**Proof.** Since $i\leftrightarrow j$, there exist $m,n\geq1$ such that
$$
P_{ji}^{(m)}>0,\qquad P_{ij}^{(n)}>0.
$$
For every $\nu\geq0$, a path from $j$ to $j$ can go first from $j$ to $i$, then from $i$ back to $i$ in $\nu$ steps, then from $i$ to $j$. Therefore
$$
P_{jj}^{(m+\nu+n)}
\geq
P_{ji}^{(m)}P_{ii}^{(\nu)}P_{ij}^{(n)}.
$$
Summing over $\nu$,
$$
\sum_{\nu=0}^{\infty}P_{jj}^{(m+\nu+n)}
\geq
P_{ji}^{(m)}P_{ij}^{(n)}
\sum_{\nu=0}^{\infty}P_{ii}^{(\nu)}.
$$
Since $i$ is recurrent,
$$
\sum_{\nu=0}^{\infty}P_{ii}^{(\nu)}=\infty
$$
by the recurrence criterion. The constants $P_{ji}^{(m)}$ and $P_{ij}^{(n)}$ are strictly positive, so the left-hand series diverges. Hence
$$
\sum_{\ell=0}^{\infty}P_{jj}^{(\ell)}=\infty,
$$
and by the same recurrence criterion, $j$ is recurrent. $\square$

## 8. Poisson Interarrival Times Are I.I.D. Exponential

**Theorem.** For a Poisson process of rate $\lambda$, the interarrival times are i.i.d. exponential random variables with mean $1/\lambda$.

**Proof.** Let $T_1$ be the first arrival time. Then
$$
\mathbb{P}(T_1>t)=\mathbb{P}(X(t)=0)=e^{-\lambda t},
$$
so $T_1\sim\mathrm{Exp}(\lambda)$.

Let $T_n$ be the $n$-th interarrival time, and let $S_n=T_1+\cdots+T_n$ be the $n$-th arrival epoch. Conditional on the history up to $S_n$, the waiting time until the next arrival exceeds $t$ exactly when there are no Poisson arrivals in $(S_n,S_n+t]$. By independent and stationary increments,
$$
\mathbb{P}(T_{n+1}>t\mid \text{history up to }S_n)
=\mathbb{P}(X(t)=0)=e^{-\lambda t}.
$$
Thus every interarrival time has exponential rate $\lambda$, and each new interarrival time is independent of the past. Hence the interarrival times are i.i.d. $\mathrm{Exp}(\lambda)$.

Finally,
$$
\mathbb{E}[T_n]=\int_0^\infty \mathbb{P}(T_n>t)\,dt
=\int_0^\infty e^{-\lambda t}\,dt
=\frac{1}{\lambda}.
$$
$\square$

## 9. Reflected Random Walk on Non-Negative Integers

**Theorem.** Consider the Markov chain on $\mathbb{N}$ with
$$
P_{01}=1,\qquad P_{i,i+1}=p,\qquad P_{i,i-1}=q,\quad i>0,\qquad p+q=1,
$$
and assume $0<p,q<1$. Then:

- if $p<q$, the chain is positive recurrent;
- if $p=q=1/2$, the chain is null recurrent;
- if $p>q$, the chain is transient.

When $p<q$, the stationary distribution is
$$
\pi_0=\frac{q-p}{1+q-p}=\frac{q-p}{2q},
$$
and, for $i\geq1$,
$$
\pi_i=\pi_0\frac{p^{i-1}}{q^i}.
$$

**Proof.** First study recurrence. Let
$$
h_i=\mathbb{P}_i(T_0<\infty)
$$
be the probability of ever hitting $0$ starting from $i$. Then $h_0=1$ and, for $i\geq1$,
$$
h_i=ph_{i+1}+qh_{i-1}.
$$
The general solution is
$$
h_i=
\begin{cases}
A+B(q/p)^i, & p\neq q,\\
A+Bi, & p=q.
\end{cases}
$$
Since $0\leq h_i\leq1$ and $h_0=1$:

- if $p<q$, then $(q/p)^i\to\infty$, so boundedness forces $B=0$ and $h_i=1$;
- if $p=q$, boundedness forces $B=0$ and $h_i=1$;
- if $p>q$, the bounded solution satisfying $h_0=1$ and $h_i\to0$ as $i\to\infty$ is $h_i=(q/p)^i<1$.

Thus the chain is recurrent for $p\leq q$ and transient for $p>q$.

Now solve for a stationary distribution. The balance equations are
$$
\pi_0=q\pi_1,
$$
and for $i\geq1$,
$$
\pi_i=p\pi_{i-1}+q\pi_{i+1}.
$$
Equivalently, using birth-death detailed balance,
$$
\pi_0P_{01}=\pi_1P_{10},\qquad
\pi_iP_{i,i+1}=\pi_{i+1}P_{i+1,i}\quad (i\geq1).
$$
Hence
$$
\pi_1=\frac{\pi_0}{q},\qquad
\pi_{i+1}=\frac{p}{q}\pi_i,
$$
so
$$
\pi_i=\pi_0\frac{p^{i-1}}{q^i},\qquad i\geq1.
$$
Normalize:
$$
\begin{aligned}
1
&=\pi_0+\sum_{i=1}^{\infty}\pi_0\frac{p^{i-1}}{q^i}\\
&=\pi_0\left[1+\frac{1}{q}\sum_{i=1}^{\infty}\left(\frac{p}{q}\right)^{i-1}\right].
\end{aligned}
$$
The geometric series converges iff $p<q$. In that case,
$$
1=\pi_0\left(1+\frac{1}{q-p}\right)
=\pi_0\frac{1+q-p}{q-p},
$$
so
$$
\pi_0=\frac{q-p}{1+q-p}.
$$
Therefore the recurrent case $p<q$ is positive recurrent. When $p=q$, the chain is recurrent but has no normalizable stationary distribution, so it is null recurrent. When $p>q$, it is transient. Because the chain has period $2$, the stationary distribution for $p<q$ gives steady-state time proportions, while ordinary one-step limiting probabilities oscillate by parity. $\square$

## 10. Formal Renewal Identity for $\mathbb{E}[S_{N(t)+1}]$

**Theorem.** For a renewal process with $\mu=\mathbb{E}[X_1]<\infty$,
$$
\mathbb{E}[S_{N(t)+1}]=\mathbb{E}[X_1](M(t)+1).
$$

**Proof.** This is the same identity as in Theorem 2, now proved through Wald's equation. Let
$$
T=N(t)+1=\min\{n\geq1:S_n>t\}.
$$
With respect to $\mathcal{F}_n=\sigma(X_1,\ldots,X_n)$, $T$ is a stopping time because
$$
\{T\leq n\}=\{S_n>t\}\in\mathcal{F}_n.
$$
Also $T<\infty$ a.s. and
$$
\mathbb{E}[T]=\mathbb{E}[N(t)+1]=M(t)+1<\infty.
$$
By Wald's first equation for i.i.d. nonnegative increments with finite mean,
$$
\mathbb{E}[S_T]
=\mathbb{E}\left[\sum_{r=1}^{T}X_r\right]
=\mathbb{E}[T]\mathbb{E}[X_1].
$$
Since $T=N(t)+1$, this becomes
$$
\mathbb{E}[S_{N(t)+1}]
=\mathbb{E}[X_1](M(t)+1).
$$
$\square$

## 11. Conditional Poisson Counts: Smaller and Larger Time Horizons

**Theorem.** Let $X(t)$ be a Poisson process of rate $\lambda$.

For $0<u<t$ and $0\leq k\leq n$,
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=
\binom{n}{k}\left(\frac{u}{t}\right)^k
\left(1-\frac{u}{t}\right)^{n-k}.
$$

For $0<t<u$ and $0\leq n\leq k$,
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=
e^{-\lambda(u-t)}
\frac{[\lambda(u-t)]^{k-n}}{(k-n)!}.
$$

**Proof.** Case (i): $0<u<t$. This is Theorem 6 with $s=u$:
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=
\frac{\mathbb{P}[X(u)=k,\ X(t)-X(u)=n-k]}{\mathbb{P}[X(t)=n]}.
$$
Using independent Poisson increments gives the binomial expression above.

Case (ii): $0<t<u$. If $X(t)=n$ and $X(u)=k$, then there must be $k-n$ arrivals in $(t,u]$. Since $X(u)-X(t)$ is independent of $X(t)$ and has distribution $\mathrm{Poisson}(\lambda(u-t))$,
$$
\begin{aligned}
\mathbb{P}[X(u)=k\mid X(t)=n]
&=\mathbb{P}[X(u)-X(t)=k-n\mid X(t)=n]\\
&=\mathbb{P}[X(u)-X(t)=k-n]\\
&=e^{-\lambda(u-t)}\frac{[\lambda(u-t)]^{k-n}}{(k-n)!}.
\end{aligned}
$$
If $k<n$ in this second case, the probability is $0$. $\square$

## 12. Almost-Sure Renewal Rate

**Theorem.** If $\mu=\mathbb{E}[X_1]\in(0,\infty)$, then
$$
\lim_{t\to\infty}\frac{N(t)}{t}=\frac{1}{\mu}
\qquad\text{almost surely.}
$$

**Proof.** Since the interarrival times are positive and finite, $S_n\to\infty$ almost surely, hence $N(t)\to\infty$ as $t\to\infty$. By definition of $N(t)$,
$$
S_{N(t)}\leq t<S_{N(t)+1}.
$$
For $N(t)>0$, divide by $N(t)$:
$$
\frac{S_{N(t)}}{N(t)}
\leq
\frac{t}{N(t)}
<
\frac{S_{N(t)+1}}{N(t)}
=
\frac{S_{N(t)+1}}{N(t)+1}\cdot\frac{N(t)+1}{N(t)}.
$$
As $t\to\infty$, $N(t)\to\infty$. By the strong law of large numbers,
$$
\frac{S_{N(t)}}{N(t)}\to\mu,
\qquad
\frac{S_{N(t)+1}}{N(t)+1}\to\mu
\qquad\text{a.s.}
$$
Also
$$
\frac{N(t)+1}{N(t)}\to1.
$$
The squeeze theorem gives
$$
\frac{t}{N(t)}\to\mu
\qquad\text{a.s.}
$$
Taking reciprocals,
$$
\frac{N(t)}{t}\to\frac{1}{\mu}
\qquad\text{a.s.}
$$
$\square$

## Source Links

- [[sources/exams-theorems|Exams Theorems]]
- [[sources/lecture-notes-ch3|Chapter 3 - Long Run Behaviour of Markov Chains]]
- [[sources/lecture-notes-ch4|Chapter 4 - Poisson Processes]]
- [[sources/lecture-notes-ch5|Chapter 5 - Renewal Phenomena]]

