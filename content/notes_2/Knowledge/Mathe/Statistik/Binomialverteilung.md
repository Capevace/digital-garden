Die **Binomialverteilung** ist eine der wichtigsten diskreten Verteilungen. Ein binomialverteiltes Zufallsexperiment entsteht durch n-fache Wiederholung eines Bernoulli Experiments. Man unterscheidet also nur zwischen Erfolg und Nicht-Erfolg.

#### Formel
$n$ ist die *Größe der Stichprobe*
$k$ ist die *Anzahl der Erfolge*
$p$ ist die *Wahrscheinlichkeit des Erfolgs*


$$
f(k) = P(X = k) = b(n, p, k) = 
\begin{cases}
    \binom{n}{k} * p^k * (1-p)^{n-k}, \quad & k \in \{0, 1, 2, ..., n\}
	\\\\
    \; 0, & sonst
	\\
\end{cases}
$$

---

### Verteilungsfunktion der Binomialverteilung
$$
F(X \le n) = \sum_{k=0}^{n} f(k)
$$

Zum Beispiel:
$$
P(X \le 2) = P(X = 0) + P(X = 1) + P(X = 2)
$$

### [[Erwartungswert]] der Binomialverteilung
$$
E[X] = n * p
$$

**Herleitung**

$E[X_i]=\sum_{k=0}^{1}k·P(Xi =k)=0·P(Xi =0)+1·P(Xi =1)=0·(1−p)+1·p=p$
$E[Z] = E[\sum_{k=1}^{n} X_i] = \sum_{k=1}^{n} E[X_i]= \sum_{k=1}^{n}p = n*p$
### Varianz der Binomialverteilung
$$
V[X] = n * p * (1-p)
$$

### Standardabweichung Binomialverteilung
$$
s = \sqrt{V[X]}
$$