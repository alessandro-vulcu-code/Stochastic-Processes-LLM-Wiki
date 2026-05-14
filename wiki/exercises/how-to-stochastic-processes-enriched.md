---
type: exercise
tags: [exercise, exam-prep, markov-chains, poisson-process, renewal-process, gobackn-protocol]
sources: [how-to-stochastic-processes, lecture-notes-ch2, lecture-notes-ch4, lecture-notes-ch5, lecture-notes-ch6]
related: [markov-chain, poisson-process, renewal-process, renewal-reward-process, gobackn-protocol]
---

# How To Stochastic Processes - Appunto Completo

Questo appunto rielabora la trascrizione `raw/How To Stochastic Processes _240630_183444 (1).md` fondendo i passaggi originali con le spiegazioni mancanti. L'obiettivo non e' aggiungere teoria lunga, ma rendere chiaro perche' si fa ogni passaggio e quale risultato della wiki lo giustifica.

Riferimenti generali: [[wiki/sources/how-to-stochastic-processes]], [[wiki/sources/lecture-notes-ch2]], [[wiki/sources/lecture-notes-ch4]], [[wiki/sources/lecture-notes-ch5]], [[wiki/sources/lecture-notes-ch6]].

## Catene di Markov

Negli esercizi sulle catene di Markov conviene partire sempre dal grafo. Il grafo permette di vedere subito quali stati comunicano, quali classi sono chiuse, se ci sono stati assorbenti e se una classe e' periodica. Dopo questa lettura scegli lo strumento:

- per distribuzioni a tempo finito: potenze di $P$;
- per steady state: risolvi $\pi=\pi P$ e $\sum_i\pi_i=1$;
- per tempi medi di primo passaggio: equazioni di primo passo;
- per assorbimento: matrice fondamentale;
- per limiti in catene riducibili: probabilita' di assorbimento nelle classi ricorrenti.

Riferimenti: [[wiki/concepts/markov-chain]], [[wiki/concepts/stationary-distribution]], [[wiki/theorems/markov-chain-factorization]], [[wiki/theorems/mean-first-passage-time]], [[wiki/theorems/fundamental-matrix]], [[wiki/theorems/transient-to-recurrent-limit]].

### Steady State e Tempi Medi di Ritorno

Considera la catena con matrice

$$
P =
\begin{pmatrix}
0.5 & 0.3 & 0.2 \\
0.2 & 0.2 & 0.6 \\
1 & 0 & 0
\end{pmatrix},
\qquad X(0)=3.
$$

Il primo passo e disegnare il grafo:

- dallo stato 1 si va in 1 con probabilita' $0.5$, in 2 con $0.3$, in 3 con $0.2$;
- dallo stato 2 si va in 1 con $0.2$, in 2 con $0.2$, in 3 con $0.6$;
- dallo stato 3 si va in 1 con probabilita' $1$.

La distribuzione stazionaria $\pi=(\pi_1,\pi_2,\pi_3)$ soddisfa

$$
\pi=\pi P.
$$

Questa equazione significa che, in equilibrio, la massa probabilistica che trovi in ogni stato e' uguale alla massa che arriva in quello stato da tutti gli altri stati. In pratica si leggono le colonne di $P$. Per esempio:

$$
\pi_2=0.3\pi_1+0.2\pi_2,
\qquad
\pi_3=0.2\pi_1+0.6\pi_2.
$$

Serve anche la normalizzazione:

$$
\pi_1+\pi_2+\pi_3=1.
$$

Il sistema completo sarebbe

$$
\begin{cases}
\pi_1=0.5\pi_1+0.2\pi_2+\pi_3,\\
\pi_2=0.3\pi_1+0.2\pi_2,\\
\pi_3=0.2\pi_1+0.6\pi_2,\\
\pi_1+\pi_2+\pi_3=1.
\end{cases}
$$

Di solito una delle equazioni $\pi=\pi P$ e' ridondante, quindi puoi usarne due piu' la normalizzazione. La soluzione e'

$$
\pi_1=\frac59,\qquad
\pi_2=\frac5{24},\qquad
\pi_3=\frac{17}{72}.
$$

I tempi medi di ritorno si ricavano da

$$
m_i=\frac1{\pi_i}.
$$

Quindi:

$$
\theta_{11}=m_1=\frac95,\qquad
\theta_{22}=m_2=\frac{24}{5},\qquad
\theta_{33}=m_3=\frac{72}{17}.
$$

Il motivo e' intuitivo: se nel lungo periodo passi una frazione $\pi_i$ del tempo nello stato $i$, allora tra due visite consecutive a $i$ passano in media $1/\pi_i$ passi. Questo e' l'uso pratico del [[wiki/theorems/basic-limit-theorem|Basic Limit Theorem]].

### Tempi Medi e Varianza del Primo Passaggio

Per il tempo medio di primo passaggio da $i$ a $j$, con $i\ne j$, si usa la formula di primo passo:

$$
\theta_{ij}=1+\sum_{k\ne j}p_{ik}\theta_{kj}.
$$

Il termine $1$ e il passo appena fatto. Se con quel passo arrivi direttamente in $j$, il tempo residuo e zero. Se invece vai in uno stato $k\ne j$, da quel momento il tempo medio residuo e $\theta_{kj}$. Questa e' la [[wiki/theorems/mean-first-passage-time|Mean First Passage Time]].

Nella trascrizione compare, per esempio, il primo passaggio da 3 a 1:

$$
\begin{cases}
\theta_{31}=1+p_{32}\theta_{21}+p_{33}\theta_{31}, \\
\theta_{21}=1+p_{22}\theta_{21}+p_{23}\theta_{31}.
\end{cases}
$$

Il target e lo stato 1, quindi nelle somme non compaiono termini del tipo $\theta_{11}$: quando arrivi a 1 ti fermi.

Per la varianza conviene non memorizzare una formula isolata. Definisci

$$
m_i=E_i[T_j],\qquad s_i=E_i[T_j^2],
$$

dove $T_j$ e' il tempo di primo arrivo in $j$. Il primo momento soddisfa

$$
m_i=1+\sum_{k\ne j}p_{ik}m_k.
$$

Il secondo momento soddisfa

$$
s_i=1+2\sum_{k\ne j}p_{ik}m_k+\sum_{k\ne j}p_{ik}s_k.
$$

Infatti, se dopo il primo passo vai in $k\ne j$, allora $T_j=1+T_j^{(k)}$, quindi

$$
T_j^2=(1+T_j^{(k)})^2=1+2T_j^{(k)}+(T_j^{(k)})^2.
$$

Una volta trovati $m_i$ e $s_i$:

$$
\operatorname{Var}_i(T_j)=s_i-m_i^2.
$$

### Probabilita' Condizionata su una Traiettoria

Considera

$$
P[X(1)=1,\ X(3)=1 \mid X(2)=2],
\qquad X(0)=3.
$$

La traiettoria nel numeratore e'

| $t$ | 0 | 1 | 2 | 3 |
|---|---:|---:|---:|---:|
| state | 3 | 1 | 2 | 1 |

Per la proprieta' di Markov, la probabilita' di questa traiettoria e il prodotto delle transizioni:

$$
p_{31}p_{12}p_{21}.
$$

Pero' essendo una probabilita' condizionata bisogna dividere per la probabilita' della condizione $X(2)=2$ partendo da $X(0)=3$. Questa probabilita' include tutte le traiettorie che in due passi portano da 3 a 2, quindi e'

$$
p_{32}^{(2)}=(P^2)_{32}.
$$

Quindi:

$$
P[X(1)=1,\ X(3)=1 \mid X(2)=2]
=
\frac{p_{31}p_{12}p_{21}}{p_{32}^{(2)}}.
$$

Il secondo esempio e'

$$
P[X(2)=2 \mid X(1)=1,\ X(3)=1].
$$

Qui il numeratore e ancora la traiettoria completa

$$
p_{31}p_{12}p_{21}.
$$

Il denominatore invece fissa $X(1)=1$ e $X(3)=1$, ma lascia libero $X(2)$. Partendo da $X(0)=3$, serve andare da 3 a 1 in un passo e poi da 1 a 1 in due passi:

$$
p_{31}p_{11}^{(2)}.
$$

Percio'

$$
P[X(2)=2 \mid X(1)=1,\ X(3)=1]
=
\frac{p_{31}p_{12}p_{21}}{p_{31}p_{11}^{(2)}}.
$$

Riferimento: [[wiki/theorems/markov-chain-factorization]].

### Distribuzioni $X_1$, $X_2$, $X_{500}$

Se l'esercizio chiede di disegnare il diagramma e trovare $X_1$, $X_2$, $X_{500}$ dato $X_0=0$, stai lavorando con distribuzioni a tempo finito.

Se parti sicuramente dallo stato 0, la distribuzione iniziale e'

$$
\alpha=(1,0,0).
$$

Allora:

$$
X_1=\alpha P.
$$

Nel documento:

$$
X_1=(0.2,\ 0.4,\ 0.4).
$$

Poi:

$$
X_2=X_1P=(0.4,\ 0.44,\ 0.16).
$$

In generale:

$$
X_n=\alpha P^n.
$$

Per $X_{500}$ puoi sostituire con $\pi$ solo quando la catena converge alla stazionaria, cioe' tipicamente in una classe finita irriducibile e aperiodica. Se la catena e' periodica, $P^n$ puo' oscillare e non avere limite. Riferimento: [[wiki/theorems/limiting-distribution-regular-markov-chain]].

### Numero Medio di Visite

Nel documento compare

$$
W_{ij}^{(m)}=E\left[\sum_{k=0}^{m-1}I\{X_k=j\}\mid X_0=i\right].
$$

Questa quantita' e il numero medio di visite allo stato $j$ nei primi $m$ istanti, partendo da $i$. Si calcola sommando le probabilita' di essere in $j$ ai vari tempi:

$$
W_{ij}^{(m)}=\sum_{\ell=0}^{m-1}p_{ij}^{(\ell)}.
$$

Nel caso $m=3$ della trascrizione si sommano $P^0$, $P^1$ e $P^2$:

$$
W_{0j}^{(3)}
=p_{0j}^{(0)}+p_{0j}^{(1)}+p_{0j}^{(2)}.
$$

Quindi:

$$
\begin{cases}
j=0: & 1+0.2+0.4, \\
j=1: & 0+0.4+0.44, \\
j=2: & 0+0.4+0.16.
\end{cases}
$$

e

$$
W_{0j}^{(3)}
=
\begin{pmatrix}
1.6\\
0.84\\
0.56
\end{pmatrix}.
$$

Per $m$ molto grande, se la catena ha distribuzione stazionaria $\pi$, vale l'approssimazione

$$
W_{0j}^{(m)}\simeq m\pi_j.
$$

Nel documento:

$$
\pi =
\left(
\frac{10}{27},
\frac{4}{9},
\frac{5}{27}
\right),
$$

quindi

$$
W_{0j}^{(5000)}
\simeq
\begin{pmatrix}
\frac{10}{27}\cdot 5000 \\
\frac{4}{9}\cdot 5000 \\
\frac{5}{27}\cdot 5000
\end{pmatrix}
=
\begin{pmatrix}
1852\\
2222\\
926
\end{pmatrix}.
$$

Il ragionamento e: se nel lungo periodo passi una frazione $\pi_j$ del tempo nello stato $j$, in 5000 passi ti aspetti circa $5000\pi_j$ visite.

### Caso con Stato Assorbente

Se uno stato e' assorbente, per esempio lo stato 2, il numero medio di visite allo stato assorbente diverge:

$$
\lim_{m\to\infty}W_{02}^{(m)}=\infty.
$$

Per gli stati transitori invece il numero medio totale di visite e finito. Con

$$
P =
\begin{pmatrix}
0.2 & 0.6 & 0.2 \\
0.6 & 0.2 & 0.2 \\
0 & 0 & 1
\end{pmatrix},
$$

la parte transitoria e'

$$
Q=
\begin{pmatrix}
0.2&0.6\\
0.6&0.2
\end{pmatrix}.
$$

La matrice fondamentale e'

$$
W=(I-Q)^{-1}=I+Q+Q^2+\cdots.
$$

Il documento imposta le stesse equazioni componente per componente:

$$
\begin{cases}
W_{00}=0.2W_{00}+0.6W_{10}+1,\\
W_{10}=0.6W_{00}+0.2W_{10}.
\end{cases}
$$

Il termine $+1$ nella prima equazione compare perche' partendo da 0 hai gia' una visita allo stato 0 al tempo 0. Risolvendo:

$$
W_{00}=\frac{20}{7},
\qquad
W_{10}=\frac{15}{7}.
$$

Per simmetria:

$$
W_{11}=\frac{20}{7},
\qquad
W_{01}=\frac{15}{7}.
$$

Il tempo medio prima dell'assorbimento partendo da 0 e la somma delle visite medie agli stati transitori:

$$
E[T_{\text{ass}}\mid X_0=0]
=W_{00}+W_{01}
=\frac{35}{7}=5.
$$

Si puo' ottenere lo stesso risultato con first-step analysis:

$$
\begin{cases}
V_0=1+p_{00}V_0+p_{01}V_1,\\
V_1=1+p_{10}V_0+p_{11}V_1.
\end{cases}
$$

Riferimenti: [[wiki/theorems/fundamental-matrix]], [[wiki/theorems/mean-absorption-time]].

### Catena Grande: Classi, Limiti e Tempi di Passaggio

Nel template della catena a 5 stati la matrice e'

$$
P =
\begin{pmatrix}
0 & 0 & 0 & 1 & 0 \\
0 & 0.4 & 0 & 0 & 0.6 \\
0 & 0 & 0.5 & 0.2 & 0.3 \\
1 & 0 & 0 & 0 & 0 \\
0 & 0.3 & 0 & 0 & 0.7
\end{pmatrix}.
$$

Il procedimento e sempre:

1. disegna il grafo;
2. trova le classi comunicanti;
3. identifica quali classi sono chiuse;
4. classifica gli stati transitori e ricorrenti;
5. calcola le probabilita' di assorbimento nelle classi chiuse;
6. dentro ogni classe chiusa trova la stazionaria;
7. costruisci limiti o medie di Cesaro.

Nel documento le classi sono:

- $A$: classe positiva ricorrente periodica, periodo $d=2$;
- $B$: classe transitoria;
- $C$: classe positiva ricorrente aperiodica.

Le probabilita' di assorbimento a partire dallo stato 2 sono:

$$
\pi_2(A)=\frac25,
\qquad
\pi_2(C)=\frac35.
$$

Se una classe e' periodica, $\lim_{m\to\infty}P^m$ puo' non esistere. Per questo negli esami spesso chiedono

$$
\lim_{m\to\infty}\frac1m\sum_{k=0}^{m-1}P^k.
$$

Questa media elimina le oscillazioni periodiche. Nel documento:

$$
\lim_{m\to\infty}\frac{1}{m}\sum_{k=0}^{m-1}P^k
=
\begin{pmatrix}
\frac12 & 0 & 0 & \frac12 & 0 \\
0 & \frac13 & 0 & 0 & \frac23 \\
\frac15 & \frac15 & 0 & \frac15 & \frac25 \\
\frac12 & 0 & 0 & \frac12 & 0 \\
0 & \frac13 & 0 & 0 & \frac23
\end{pmatrix}.
$$

Per la classe chiusa $C=\{1,4\}$, si risolve la stazionaria interna:

$$
\begin{cases}
\pi_1=0.4\pi_1+0.3\pi_4,\\
\pi_4=0.6\pi_1+0.7\pi_4,\\
\pi_1+\pi_4=1.
\end{cases}
$$

La soluzione e'

$$
\pi_1=\frac13,
\qquad
\pi_4=\frac23.
$$

Se parti da uno stato transitorio e arrivi in $C$ con probabilita' $3/5$, allora le probabilita' limite associate agli stati di $C$ sono pesate:

$$
\pi_{21}=\frac35\cdot\frac13,
\qquad
\pi_{24}=\frac35\cdot\frac23.
$$

Questo e il contenuto pratico del [[wiki/theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]].

Per il primo passaggio verso lo stato 4:

- se da uno stato non esiste un cammino verso 4, il tempo medio e $\infty$;
- se sei nella classe chiusa che contiene 4, usi first-step analysis;
- per il ritorno a 4, usi $1/\pi_4$.

Nel documento:

$$
m_{i4}
=
\left[
\infty,\ \frac{1}{1-0.4},\ \infty,\ \infty,\ \frac{1}{\pi_4}
\right]
=
\left[
\infty,\ \frac53,\ \infty,\ \infty,\ \frac32
\right].
$$

Per lo stato 1:

$$
V_{14}=1+p_{11}V_{14}+p_{14}\cdot0
\quad\Rightarrow\quad
V_{14}=\frac{1}{1-p_{11}}=\frac53.
$$

Per lo stato 4, il tempo medio di ritorno e

$$
V_{44}=\frac1{\pi_4}=\frac32.
$$

## Go-Back-N

Gli esercizi Go-Back-N sono esercizi di reward/time. Un pacchetto corretto produce reward 1; un errore fa perdere tempo, tipicamente $m$ slot, dove $m$ e il round-trip time. Il throughput e quindi

$$
\eta=\frac{\text{reward medio per ciclo}}{\text{tempo medio per ciclo}}.
$$

Riferimenti: [[wiki/concepts/gobackn-protocol]], [[wiki/theorems/gobackn-throughput-markov-errors]], [[wiki/theorems/transition-generating-matrix-method]], [[wiki/theorems/renewal-reward-theorem]].

### Esempio con Matrice del Canale Data

Nel documento:

$$
P =
\begin{pmatrix}
0.98 & 0.02 \\
0.1 & 0.9
\end{pmatrix}.
$$

Gli stati sono:

- $G$: good state;
- $B$: bad state.

Con $m=2$ serve la matrice a due passi:

$$
P^2 =
\begin{pmatrix}
0.9624 & 0.0376 \\
0.188 & 0.812
\end{pmatrix}.
$$

Il throughput con feedback senza errori e'

$$
\eta=
\frac{p_{10}^{(2)}}{p_{10}^{(2)}+2p_{01}}.
$$

Qui $p_{10}^{(2)}$ e la probabilita' che, partendo da bad, dopo due slot il canale sia good. Il termine $2p_{01}$ rappresenta il costo temporale degli errori che si innescano quando si passa da good a bad.

Con feedback soggetto a errore iid $\delta$, il documento usa:

$$
\eta =
\frac{(1-\delta)p_{10}^{(m)}}
{(1-\delta+m\delta)p_{10}^{(m)}
+m\left[(1-\delta)p_{01}+\delta p_{01}^{(m)}\right]}.
$$

La logica resta la stessa: al numeratore ci sono i successi utili, al denominatore il tempo medio consumato includendo retransmission e feedback sbagliati.

### Canale Markov per una Parte del Tempo e iid per il Resto

Se il canale alterna:

- $1{,}000{,}000$ slot Markov;
- $2{,}000{,}000$ slot iid;

allora il throughput finale e una media pesata sui tempi:

$$
\eta_{\text{finale}}
=\frac13\eta_{\text{Markov}}+\frac23\eta_{\text{iid}}.
$$

Per un canale iid con probabilita' di errore $\varepsilon$:

$$
\eta_{\text{iid}}
=
\frac{1-\varepsilon}{1-\varepsilon+m\varepsilon}.
$$

Nel documento, con $\varepsilon=0.01$, si ottiene circa

$$
T_{\text{i.i.d.}}\simeq0.98.
$$

Poi:

$$
\mu_{\text{final}}
=\frac13T_{\text{Markov}}+\frac23T_{\text{i.i.d.}}
=0.928.
$$

### Ricavare le Probabilita' da Slot Consecutivi

Nel documento sono dati:

$$
p_B=\pi_1=0.02,
\qquad
p_{01}=\frac1{100}=0.01,
\qquad
m=2.
$$

Se la durata media di una sequenza di good slot e 100, allora la probabilita' di uscire da good e

$$
p_{01}=\frac1{100}.
$$

Per una catena a due stati:

$$
\pi_1=\frac{p_{01}}{p_{01}+p_{10}}.
$$

Da cui:

$$
p_{10}
=\frac{p_{01}(1-\pi_1)}{\pi_1}
=0.49.
$$

Quindi:

$$
p_{11}=1-p_{10}=0.51.
$$

Il grafo diventa:

- $G\to G$: $0.99$;
- $G\to B$: $0.01$;
- $B\to G$: $0.49$;
- $B\to B$: $0.51$.

Senza protocollo, il throughput e semplicemente la probabilita' stazionaria di good:

$$
\eta_{\text{no protocol}}=\pi_0=\frac{p_{10}}{p_{10}+p_{01}}\simeq0.98.
$$

## Processi di Poisson

Gli esercizi sui processi di Poisson si risolvono quasi sempre con quattro idee:

1. incrementi indipendenti;
2. conteggi Poisson con parametro $\lambda t$;
3. superposizione: la somma di Poisson indipendenti e Poisson;
4. dato un totale, la ripartizione in sottointervalli o sottoprocessi e binomiale.

Riferimenti: [[wiki/concepts/poisson-process]], [[wiki/theorems/superposition-theorem]], [[wiki/theorems/thinning-theorem]], [[wiki/theorems/binomial-conditional-distribution]], [[wiki/theorems/conditional-arrival-times-uniform]].

### Singolo Processo Condizionato sul Conteggio Futuro

Per

$$
P[X(\mu)=k\mid X(t)=m],
\qquad 0<\mu<t,
$$

vale

$$
P[X(\mu)=k \mid X(t)=m]
=
\binom{m}{k}
\left(\frac{\mu}{t}\right)^k
\left(1-\frac{\mu}{t}\right)^{m-k}.
$$

Il motivo e che, dato $X(t)=m$, gli $m$ arrivi sono distribuiti come punti uniformi in $(0,t]$. Ciascun punto cade in $(0,\mu]$ con probabilita' $\mu/t$. Riferimento: [[wiki/theorems/binomial-conditional-distribution]].

### Due Processi di Poisson Indipendenti

Per due processi indipendenti $X_1,X_2$ con tassi $d_1,d_2$:

$$
X_1(t)+X_2(t)\sim\operatorname{Poisson}((d_1+d_2)t).
$$

Dato il totale, ogni arrivo ha probabilita'

$$
\frac{d_1}{d_1+d_2}
$$

di appartenere al primo processo. Se pero' guardi solo $X_1(\mu)$ con $\mu<t$, la probabilita' che un arrivo totale in $[0,t]$ sia sia del processo 1 sia cada in $[0,\mu]$ e

$$
\frac{d_1\mu}{(d_1+d_2)t}.
$$

Quindi:

$$
P[X_1(\mu)=k \mid X_1(t)+X_2(t)=m]
=
\binom{m}{k}
\left(\frac{d_1\mu}{(d_1+d_2)t}\right)^k
\left(\frac{d_1(t-\mu)+d_2t}{(d_1+d_2)t}\right)^{m-k}.
$$

### Condizionare su un Conteggio Parziale

Con $d_1=d_2=1$, considera:

$$
P[X_1(2)+X_2(2)=4\mid X_1(1)=1].
$$

La condizione dice che un arrivo di $X_1$ in $[0,1]$ e gia' fissato. Per arrivare a 4 arrivi totali in $[0,2]$, servono altri 3 arrivi nelle parti ancora libere:

- $X_1$ in $(1,2]$;
- $X_2$ in $(0,2]$.

Il parametro totale e

$$
d_1(2-1)+d_2\cdot2=1+2=3.
$$

Percio':

$$
P[X_1(2)+X_2(2)-X_1(1)=3]
=
e^{-3}\frac{3^3}{3!}.
$$

Regola pratica: togli dal conteggio richiesto cio' che e' gia' imposto dal condizionamento, poi calcola la Poisson sulle parti indipendenti rimaste.

### Esempi Condizionati

Considera:

$$
P[X_2(1)=2\mid X_1(1)+X_2(1)=2,\ X_1(2)=0].
$$

La condizione $X_1(2)=0$ implica $X_1(1)=0$. Se nel primo intervallo il totale e 2 e nessuno viene da $X_1$, allora necessariamente $X_2(1)=2$. Quindi questa probabilita' condizionata e 1.

La trascrizione semplifica a

$$
P[X_2(1)=2]=e^{-1}\frac{1^2}{2!},
$$

ma questa e la probabilita' non condizionata. In questo punto il manoscritto sembra saltare una condizione importante.

Un secondo esempio:

$$
P[X_1(1)+X_2(1)=2\mid X_1(2)=1].
$$

Dato $X_1(2)=1$, l'unico arrivo di $X_1$ in $[0,2]$ cade nella prima meta' con probabilita' $1/2$ e nella seconda meta' con probabilita' $1/2$. Quindi:

- se cade in $(0,1]$, serve $X_2(1)=1$;
- se cade in $(1,2]$, serve $X_2(1)=2$.

La probabilita' e

$$
\frac12P[X_2(1)=1]+\frac12P[X_2(1)=2].
$$

Qui si usa il fatto che, dato il numero di arrivi in un intervallo, i tempi di arrivo sono uniformi. Riferimento: [[wiki/theorems/conditional-arrival-times-uniform]].

Per

$$
P[X_1(3)=3\mid X_1(2)=1],
$$

la condizione fissa 1 arrivo entro tempo 2. Per avere 3 arrivi entro tempo 3, servono 2 nuovi arrivi in $(2,3]$. Quindi:

$$
P[X_1(3)-X_1(2)=2].
$$

Si usa l'incremento indipendente del processo $X_1$ sul solo intervallo $(2,3]$.

### Visitatori in una Mostra

Supponi arrivi Poisson con

$$
\lambda=10/\text{h}
$$

e tempo di permanenza

$$
Y\sim U[20,30]\text{ min}.
$$

Per "meno di tre visitatori durante la prima mezz'ora" non serve il tempo di permanenza: si contano solo gli arrivi. In mezz'ora:

$$
\lambda t=10\cdot\frac12=5.
$$

Quindi:

$$
P[X(0.5)<3]
=
\sum_{k=0}^2 e^{-5}\frac{5^k}{k!}
=
e^{-5}\left(1+5+\frac{25}{2}\right)
\simeq0.125.
$$

Per "un visitatore nella stanza alle 8:15", il tempo trascorso e

$$
t=\frac14\text{ h}.
$$

Poiche' il tempo minimo di permanenza e 20 minuti, ogni visitatore arrivato nei primi 15 minuti e ancora dentro. Quindi il numero nella stanza coincide con il numero di arrivi:

$$
P[N(1/4)=1]
=e^{-5/2}\frac{(5/2)^1}{1!}
\simeq0.205.
$$

Per il numero di persone presenti a regime si usa il modello M/G/infinity:

$$
N\sim\operatorname{Poisson}(\lambda E[Y]).
$$

Qui

$$
E[Y]=\frac{\frac13+\frac12}{2}=\frac5{12}\text{ h}.
$$

Quindi:

$$
\lambda E[Y]=10\cdot\frac5{12}=\frac{25}{6}.
$$

Alla chiusura, dopo 10 ore, il sistema e gia' oltre la durata massima delle visite, quindi:

$$
P[N=0]=e^{-25/6}.
$$

Riferimento: [[wiki/concepts/m-g-infinity-queue]].

### Nodo con Due Link in Ingresso

Con

$$
d_1=d_2=500\text{ packets/s},
$$

in un intervallo di 3 ms ogni link ha parametro

$$
500\cdot0.003=1.5.
$$

La probabilita' di ricevere 2 pacchetti dal primo link e 1 dal secondo e, per indipendenza:

$$
e^{-1.5}\frac{1.5^2}{2!}
\cdot
e^{-1.5}\frac{1.5^1}{1!}
\simeq0.084.
$$

Per ricevere 3 pacchetti totali, si sommano i tassi:

$$
d=d_1+d_2=1000,
\qquad
dt=1000\cdot0.003=3.
$$

Quindi:

$$
P[X(3\text{ ms})=3]
=e^{-3}\frac{3^3}{3!}
\simeq0.224.
$$

Per la probabilita' di ricevere 2 pacchetti dal primo link dato che il totale e 3:

$$
P[X_1=2\mid X_1+X_2=3]
=
\binom32\left(\frac12\right)^2\left(\frac12\right)
=\frac38.
$$

La formula $\frac38$ corrisponde al condizionamento sul totale uguale a 3. Se invece si condizionasse davvero su $X_2=3$, come sembra scritto in un punto della trascrizione, non sarebbe la stessa domanda.

### Web Server e Richieste Attive

Se le richieste arrivano come Poisson con

$$
\lambda=20/\text{s}
$$

e il file ha dimensione uniforme tra 1 e 2 MB, con rate di servizio 100 Mbps piu' componente fissa 20 ms, il tempo di servizio minimo e

$$
\frac{1\text{ MB}\cdot8}{100\text{ Mbps}}+20\text{ ms}
=100\text{ ms},
$$

e il massimo e

$$
\frac{2\text{ MB}\cdot8}{100\text{ Mbps}}+20\text{ ms}
=180\text{ ms}.
$$

Il tempo medio e

$$
E[Y]=\frac{100+180}{2}\text{ ms}=140\text{ ms}=0.14\text{ s}.
$$

In steady state, il numero di richieste attive e Poisson con media

$$
\lambda E[Y]=20\cdot0.14=2.8.
$$

Quindi:

$$
P[N=k]=e^{-2.8}\frac{2.8^k}{k!}.
$$

Se invece la domanda dice: "dato che in un intervallo di durata $T$ sono arrivate $N$ richieste, qual e la probabilita' che alla fine non ce ne siano attive?", allora si usa il fatto che, condizionati sul numero totale, gli arrivi sono uniformi nell'intervallo.

Se il servizio e deterministico di durata $s$, una richiesta e completata entro fine intervallo se arriva nei primi $T-s$ secondi. La probabilita' per una richiesta e

$$
\frac{T-s}{T}.
$$

Per $N$ richieste:

$$
\left(\frac{T-s}{T}\right)^N.
$$

Nel caso della trascrizione:

$$
T=30\text{ min},\qquad s=6\text{ min},\qquad N=10,
$$

quindi:

$$
P[N(t)=0\mid X(t)=10]
=
\left(\frac{24}{30}\right)^{10}
=
\left(\frac45\right)^{10}.
$$

## Renewal

Negli esercizi renewal devi scegliere un ciclo dopo il quale il sistema ricomincia probabilisticamente come all'inizio. Poi calcoli quantita' di lungo periodo come

$$
\frac{E[\text{reward nel ciclo}]}{E[\text{durata del ciclo}]}.
$$

Riferimenti: [[wiki/concepts/renewal-process]], [[wiki/concepts/renewal-reward-process]], [[wiki/theorems/renewal-reward-theorem]].

### Coda Svuotata dal Secondo Pacchetto o da Timeout

Il sistema riceve pacchetti secondo un processo di Poisson con

$$
\lambda=1\text{ packet/s}.
$$

La coda viene svuotata quando:

1. arriva un secondo pacchetto mentre ce n'e' gia' uno in coda;
2. oppure il primo pacchetto resta in coda per 2 secondi.

Il ciclo naturale e:

```text
empty -> first packet arrives -> one packet waits -> transmit -> empty
```

Il tempo medio vuoto e il tempo medio fino al primo arrivo:

$$
E[\text{first arrival}]=\frac1\lambda=1.
$$

Dopo il primo arrivo, si aspetta il minimo tra il prossimo interarrivo $A$ e il timeout 2:

$$
\min(A,2).
$$

Con $A\sim\operatorname{Exp}(1)$:

$$
E[\min(A,2)]
=
\int_0^2P[A>t]\,dt
=
\int_0^2e^{-t}\,dt
=1-e^{-2}.
$$

Quindi la frazione di tempo in cui il sistema e vuoto e

$$
P[\text{empty}]
=
\frac{E[\text{tempo vuoto nel ciclo}]}
{E[\text{durata ciclo}]}
=
\frac{1}{1+(1-e^{-2})}
\simeq0.536.
$$

Il valore

$$
1-e^{-2}=0.864
$$

e il tempo medio della fase in cui un pacchetto sta aspettando il secondo pacchetto o il timeout.

### Delay Medio dei Pacchetti

Il delay medio per pacchetto non si calcola come frazione di tempo, ma come

$$
\frac{E[\text{attesa totale dei pacchetti in un ciclo}]}
{E[\text{numero di pacchetti trasmessi in un ciclo}]}.
$$

Nel ciclo:

- se il secondo pacchetto arriva prima di 2 secondi, vengono trasmessi 2 pacchetti;
- se scatta il timeout, viene trasmesso 1 pacchetto.

Quindi

$$
E[\text{numero pacchetti}]
=2P[A<2]+1P[A\ge2]
=2(1-e^{-2})+e^{-2}
=2-e^{-2}.
$$

L'attesa totale nel ciclo e:

- $A$ se il secondo pacchetto arriva prima del timeout;
- $2$ se scatta il timeout.

Percio'

$$
E[\text{attesa totale}]
=\int_0^2 t e^{-t}\,dt+2e^{-2}
=1-e^{-2}.
$$

Il delay medio per pacchetto e

$$
\frac{1-e^{-2}}{2-e^{-2}}
\simeq0.464\text{ s}.
$$

Il prodotto visibile nel manoscritto,

$$
0.864\cdot0.536,
$$

porta allo stesso valore perche' $0.864=1-e^{-2}$ e $0.536=1/(2-e^{-2})$.

### Esempio CSMA-like

Il link ha capacita'

$$
C=1\text{ Mbps},
$$

arrivi Poisson collettivi con

$$
\lambda=500\text{ packets/s},
$$

e pacchetti da

$$
1000\text{ bit}.
$$

Il tempo medio idle prima del prossimo arrivo e

$$
\frac1\lambda=\frac1{500}=0.002\text{ s}=2\text{ ms}.
$$

Il tempo di trasmissione e

$$
T_x=\frac{1000}{1\text{ Mbps}}
=0.001\text{ s}=1\text{ ms}.
$$

Un ciclo medio dura quindi

$$
2\text{ ms}+1\text{ ms}=3\text{ ms}.
$$

La frazione di tempo busy e

$$
\frac{1}{3},
$$

mentre la frazione idle e

$$
\frac{2}{3}.
$$

Il throughput utile medio e un pacchetto da 1000 bit ogni 3 ms:

$$
\mu=
\frac{1000\text{ bit}}{0.003\text{ s}}
\simeq333333\text{ bit/s}
=0.333\text{ Mbps}.
$$

Il valore trascritto come circa 933 Mbps non e compatibile con un link da 1 Mbps. Il dato coerente con i passaggi e un'utilizzazione di $1/3$, cioe circa $0.333$ Mbps di traffico utile.

## Checklist Finale

Per non perdersi negli esercizi:

- se vedi $\pi=\pi P$, stai cercando una distribuzione stazionaria;
- se vedi "first passage", scrivi equazioni di primo passo;
- se c'e' uno stato assorbente, separa $Q$ e usa $(I-Q)^{-1}$;
- se $P^n$ non converge per periodicita', usa la media di Cesaro;
- se in Poisson condizionano sul totale, usa una binomiale;
- se hai piu' flussi Poisson indipendenti, somma i tassi;
- se chiedono utenti/richieste attive, pensa a M/G/infinity;
- se chiedono una frazione di tempo o un throughput medio, scegli un ciclo renewal e fai reward medio diviso durata media.
