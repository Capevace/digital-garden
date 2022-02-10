---
cssclass: clean-embeds
---

##  Differentialrechnung

## Binomialkoeffizient
![[Binomialkoeffizient]]

## Interesting Facts

$1-(1 - x) = 1 - 1 + x$
und
$x-(a - b + c) = x - a + b - c$
+/- sind also invertierbar

---

$$
x^{a*b} = \big(x^a\big)^b
$$
---
$$
2x-a = 2(x-a)+a \quad \text{weil} \quad 2(x-a)+a = 2x-2a+a
$$
$2l-1 = 2(l-1)+1$

---
Wenn bei einer Summe +1 im Exponenten steht kann es nach herausgenommen und multipliziert werden.
$$
\sum_{l=1}^{\infty} x^{l + 1} \quad = \quad x * \sum_{l=1}^{\infty} x^{l}
$$

---

$$
(\frac{1}{1-x}) - 1 \; = \; \frac{x}{1-x}
$$

---

$$
\frac{a}{\frac{b}{c}} \; = \; a * \frac{c}{b}
$$

---

$$
f(x) = (a + 1) * x^a
$$
aufgeleitet:
$$
F(x) = x^{a+1}
$$

## Rechnen mit Logarithmen
$$
\begin{align}
ln(x*y)	& = ln(x) + ln(y) \\
ln(\frac{x}{y}) & = ln(x) - ln(y) \\
ln(x^{y}) & = y * ln(x) \\
ln(\prod_{k=0}^{n}{x_K}) & = \sum_{k=0}^{n}{x_K}
\end{align}
$$

## PQ-Formel
![[PQ-Formel]]

## Integralrechnung

$\int x * f(x) = x * \int f(x)$

$\int 1 - u^2 = \int 1 - \int u^2$

$[x]^o_{u} = o*x - u *x$

#todo
Mit aufnehmen https://studyflix.de/mathematik/aufleiten-3340


## Dichtefunktion
![[Dichtefunktion]]

## Lage- & Streuungsparameter
![[Lage- & Streuungsparameter]]

## Geometrische Reihe
![[Geometrische Reihe]]
## Wahrscheinlichkeitsrechnung

###  Bei k-ten Wurf das erste Mal eine 6 oben

$$
\Omega = \{1, 2, 3, 4 ...\} \\
$$
$$
P(\{k\}) = \frac{1}{6} \Big(\frac{5}{6}\Big)^{k-1}
$$

## Anzahl ungerade
$$
B = \{1, 3, 5 ...\} \\
$$
$$
\begin{align}
P(B) & = \sum_{k \epsilon B} P(\{k\}) \\
    & = \frac{1}{6} \sum_{k=1}^{\infty} \Big(\frac{5}{6}\Big)^{2k-1-1} \\
	& = \frac{1}{6} \sum_{k=1}^{\infty}  \Big(\frac{5}{6}\Big)^{2(k-1)} \\
	& = \frac{1}{6} \sum_{k=1}^{\infty}  \Big(\frac{25}{36}\Big)^{k-1} \\
	& = \frac{1}{6} \sum_{k=0}^{\infty}  \Big(\frac{25}{36}\Big)^{k} \Rightarrow \text{Geometrische Reihe} \\
	& \Rightarrow \frac{1}{6} * \frac{1}{1-\frac{25}{36}}
\end{align}
$$

## Kombinatorik / Anzahl der Möglichkeiten

###  ✅ Zurücklegen  ✅ Reihenfolge
**Beispiel** 
Zahlenschloss, jede Ziffer kann 1-9 sein und Reihenfolge ist wichtig.

**Gleichung** 
$$
N = n^k = n * n * n *...
$$

###  ❌ Zurücklegen  ✅ Reihenfolge
**Beispiel** 
Turnier mit 15 Teams, wie viele Möglichkeiten für 1.-3. Platz?
$15 * 14 * 13 = 2730 \qquad\qquad k=3, \quad n=15$

**Gleichung**
$$
\begin{align}
N & = n * (n-1) * (n-2) * (n-3) * ... * (n-k+1) \\
 & = \frac{n!}{(n-k)!}
\end{align}
$$

###  ✅ Zurücklegen  ❌ Reihenfolge
**Beispiel** 
Urne mit farbigen Bällen.

**Gleichung**
$$
\begin{align}
k! * N & = \frac{n!}{(n-k)!} \\
	 N & = \frac{n!}{k! * (n-k)!} = \binom{n}{k}
\end{align}
$$

###  ❌ Zurücklegen  ❌ Reihenfolge
**Beispiel** 
Urne mit farbigen Bällen. Bälle werden nacheinander entnommen.

**Gleichungen** 
$$
\begin{align}
N & = \binom{n+k-1}{k} \\
	& \\
	& = \frac{(n+k-1)!}{k! * (n+k-1-k)!} \\
	& \\
	& = \frac{(n+k-1)!}{k! * (n-1)!}
\end{align}
$$


 

## Rechenregeln für Wahrscheinlichkeiten
Sei Ω ein Ergebnisraum, dann gilt:
1.  $0≤P(A)≤1 \;$ für $\;A⊂Ω$,
2.  $P(∅)=0$
3.  $P(A) \le P(B)$, falls $A \subset B$ und $A,B \subset \Omega$
4.  $P(A)=1−P(A)$ mit $A=\Omega \setminus A$,
5.  $P(A_1 \cup A_2 \cup\;...\;\cup  A_k) = P(A_1) + P(A_2) + ... + P(A_k)$, 
falls $A_1,A_2,...,A_k$ paarweise disjunkt und $A_i \subset \Omega, i=1,...,k$
    
6. ==$P(A \cup B)= P(A) + P(B) − P(A\cap B)$==
7.  *Da $A \subset B$, ist $B = B \setminus A \cup A$, d.h.*
	$P(B) = P(B \setminus A) + P(A)$
	
---

### Bedingte Wahrscheinlichkeit

**Wahrscheinlichkeit A und B treffen ein**
$$
P(A \cap B) = P(A) * P_A(B)
$$

****
$$
P(A|B) = \frac{P(A \cap B)}{P(B)}
$$

**Tabelle**
![[Bildschirmfoto 2022-02-06 um 20.18.53.png]]

$$
\begin{align}
P(S \cap M) & = \frac{62}{75} 
\\
P(\bar{S} \cap M) & = \frac{13}{75} 
\\ \\
P(M \cap S) & = \frac{62}{72} 
\\
P(\bar{M} \cap S) & = \frac{10}{72} 
\\ \\
P(\bar{M} \cap \bar{S}) & = \frac{15}{28}
\end{align}
$$

## Wahrscheinlichkeitsraum
### $\sigma$-Algebra
Eine Menge $\Lambda$ von Teilmengen von $\Omega$ heißt $\sigma$-Algebra wenn gilt:

1. $\emptyset \in 𝒜 \quad \text{und} \quad \Omega \in 𝒜$
2. $A \in 𝒜 \implies A^c := (\Omega \setminus A) \in 𝒜$
3. $A, B \in 𝒜 \implies A \cup B, \; A \cap B, \; A \setminus B \in 𝒜$
4. $A_1, ..., A_n \in 𝒜 \quad n \in \mathbb{N} \implies \quad \bigcup_{i=1}^{n} A_n \quad \text{und} \quad \bigcap_{i=1}^{n} A_n \in 𝒜$

**Beispiele für $\sigma$-Algebras**
Potenzmenge  𝒫($\Omega$) = Menge aller Teilmengen von $\Omega$
𝒫($\{1, 2, 3\}$) $= \{\{\emptyset\}, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1,3\}, \{2,3\}, \{1,2,3\}\}$

### Mit Zähldichten
#todo

## Erwartungswert
![[Erwartungswert]]

## Wahrscheinlichkeitsmaß
$\Omega \ne \emptyset$ und 𝒜 ist $\sigma$-Algebra über $\Omega$

1.  $𝑃(𝐴)∈ [0,1] \quad ∀ 𝐴∈𝒜$
2.  $𝑃(∅)=0 \quad \mathsf{und} \quad𝑃(Ω)=1$
3.  $∀𝐴∈ 𝒜 \quad \mathsf{gilt:} \quad 𝑃(𝐴^C)=1−𝑃(𝐴)$
4.  $∀𝐴,𝐵∈ 𝒜 \; \mathsf{mit} \; 𝐴≤𝐵 \; \mathsf{gilt:} \quad 𝑃(𝐴)≤𝑃(𝐵)$
5.  $∀𝐴,𝐵∈ 𝒜 \; \mathsf{mit} \; 𝐴∩𝐵= ∅ \; \mathsf{gilt:} \quad$ ==$𝑃(𝐴∪𝐵)=𝑃(𝐴)+𝑃(𝐵)$==


6  ![[Bildschirmfoto 2022-02-03 um 21.11.59.png]]


### Laplacescher Wahrscheinlichkeitsraum
1. Nur endlich viele Elemente als mögliches Ergebnis ($\Omega$ nicht $\{\infty\}$)
2. Jedes der Elemente tritt mit gleicher Wahrscheinlichkeit auf

$$
P(A) = \frac{|A|}{|\Omega|}
\quad \text{für} \; A \subseteq \Omega
$$

Damit ist $\big(\Omega, P(\Omega), P\big)$ ein Wahrscheinlichkeitsraum in dem gilt:

$$
P(\{\omega\}) = \frac{1}{|\Omega|}
\quad \text{für alle } \; \omega ∈ \Omega
$$

Wenn Elemente nicht-überlappen (disjunkt sind) gilt ist P auch $\sigma$-Additiv: 
$$
\implies P\big(\bigcup_{n=1}^{\infty} A_n\big) = \sum_{n=1}^{\infty} P(A_n)
$$

## Rechnen mit Mengen
**Bedeutungen**
$A \cup B \quad$ ist die Vereinigungsmenge (+)
$A\setminus B \quad$ ist A ohne B (-)
$A \cap B \quad$ Schnittmenge (alles was sowohl in $A$ als auch in $B$ ist)

$A \subset B \quad$ A ist in B
$A \subseteq B \quad$ A ist in und gleich B

Wenn oberes der Fall:
$ $

**Kommutativgesetze**: 
$A ∪ B = B ∪ A$  
$A ∩ B = B ∩ A$  

**Assoziativgesetze**: 
$A ∪ (B ∪ C) = (A ∪ B) ∪ C$  
$A ∩ (B ∩ C) = (A ∩ B) ∩ C$  

**Distributivgesetze**: 
$A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)$  
$A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C)$  

**Verschmelzungsgesetze**: 
$A ∪ (B ∩ A) = A$  
$A ∩ (B ∪ A) = A$  

**Idempotenzgesetze**: 
$A ∪ A = A$  
$A ∩ A = A$  

**Neutralitätsgesetze**: 
$A ∪ ∅ = A$  
$A ∩ U = A$  

**Absorptionsgesetze**: 
$A ∪ U = U$  
$A ∩ ∅ = ∅$  

**Komplementariätsgesetze**: 
$A ∪ A^c = U$
$A ∩ A^c = ∅$ 

**Doppelnegationsgesetz**: 
$(A^c)^c = A$

**Gesetze von De Morgan**:
$(A ∪ B)^c = A^c ∩ B^c$
$(A ∩ B)^c = A^c ∪ B^c$