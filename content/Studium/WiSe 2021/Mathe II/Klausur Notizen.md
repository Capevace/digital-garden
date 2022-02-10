---
cssclass: clean-embeds
---

## Differentialrechnung

## Binomialkoeffizient

Der Binomialkoeffizient gibt die **Anzahl der Möglichkeiten** an, 
aus $N$ Objekten $n$ auszuwählen. ^f6735b

#### Formel

$$
\\binom{N}{n} = \frac{N!}{(N-n)! * n!}
$$

$\binom{N}{0} = 1$
$\binom{N}{1} = N$
$\binom{N}{N} = 1$
$\binom{N}{n} = 0, \quad \text{wenn} ; N \< n$

## Interesting Facts

$1-(1 - x) = 1 - 1 + x$
und
$x-(a - b + c) = x - a + b - c$
+/- sind also invertierbar

---

## $$
x^{a\*b} = \big(x^a\big)^b
$$

$$
2x-a = 2(x-a)+a \quad \text{weil} \quad 2(x-a)+a = 2x-2a+a
$$
$2l-1 = 2(l-1)+1$

---

Wenn bei einer Summe +1 im Exponenten steht kann es nach herausgenommen und multipliziert werden.
$$
\\sum\_{l=1}^{\infty} x^{l + 1} \quad = \quad x * \sum\_{l=1}^{\infty} x^{l}
$$

---

$$
(\frac{1}{1-x}) - 1 ; = ; \frac{x}{1-x}
$$

---

$$
\\frac{a}{\frac{b}{c}} ; = ; a * \frac{c}{b}
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
\\begin{align}
ln(x\*y)	& = ln(x) + ln(y) \\
ln(\frac{x}{y}) & = ln(x) - ln(y) \\
ln(x^{y}) & = y * ln(x) \\
ln(\prod\_{k=0}^{n}{x_K}) & = \sum\_{k=0}^{n}{x_K}
\\end{align}
$$

## PQ-Formel

Die **pq-Formel** ist eine Lösungsformel für quadratische Gleichungen *in Normalform*.

$$
x\_{1/2} = -\frac{p}{2} \pm \sqrt{(\frac{p}{q})^2 - q}
$$

---

````
    p   q
````

$x^2 + 6x + 5$

## Integralrechnung

$\int x * f(x) = x * \int f(x)$

$\int 1 - u^2 = \int 1 - \int u^2$

$\[x\]^o\_{u} = o\*x - u \*x$

\#todo
Mit aufnehmen https://studyflix.de/mathematik/aufleiten-3340

## Dichtefunktion

Eine Funktion ist eine Dichte, wenn gilt:

$$
f(x) \ge 0
$$ 

und 

$$
\\int\_{R}f(x) = 1
$$

## Lage- & Streuungsparameter

### [Arithmetisches Mittel](../../../Knowledge/Mathe/Statistik/Arithmetisches%20Mittel.md)

Das **arithmetische Mittel** (auch „Mittelwert“ genannt) ist eine Kennzahl, die dir angibt, wie hoch oder niedrig **die Messwerte im Durchschnitt** sind. Für die Berechnung des arithmetischen Mittels muss man einfach alle Messwerte aufaddieren und das Ergebnis durch die Anzahl der Messwerte teilen.

#### Formel

$$
\\bar{x} = \frac{1}{n} \sum\_{i=1}^{n} x_i
$$

### [Median](../../../Knowledge/Mathe/Statistik/Median.md)

**Der Wert, der genau in der Mitte einer Datenverteilung liegt, nennt sich Median oder Zentralwert.**

#### Formel

**Reelle Zahlen (Integer):**
$$
\\tilde{x}= \begin{cases}
\\frac{1}{2} (x\_{(\frac{n}{2})} + x\_{(\frac{n}{2} + 1)}) & \text{falls gerade} \\
x\_{\frac{n+1}{2}} & \text{falls ungerade} \\
\\end{cases}
$$

**Nicht reelle Zahlen (Float):**
$$
\\tilde{x} = x\_{(\[\\frac{n}{2}\])}
$$

$\[\\text{ | }\] = \text{Aufrundungsfunktion}$ 

### Aufgaben-Beispiel

Berechnen Sie den theoretischen Median:

$F (median) = 0.5 \implies median = F^{−1}(0.5)$. 

Wegen dem in 35.iv blau markierten Teil gilt 
$median = F^{−1}(0.5) = 2$.

### [Empirische Spannbreite (Varianzbreite)](../../../Knowledge/Mathe/Statistik/Empirische%20Spannbreite%20%28Varianzbreite%29.md)

**Die emirische Spannbreite ist die Differenz zwischen dem größten und dem kleinsten Messwert.**

Da die Spannweite nur aus den zwei Extremwerten berechnet wird, ist sie nicht robust gegenüber Ausreißern.

#### Formel

$x\_{max}$ ist der *größte Messwert*
$x\_{min}$ ist der *kleinste Messwert*
–
$$
r = x\_{\text{max}} - x\_{\text{min}} = x\_{n} - x\_{1}
$$

### [Empirische Varianz](../../../Knowledge/Mathe/Statistik/Empirische%20Varianz.md)

**Die empirische Varianz berechnet die mittlere quadratische Abweichung der gemessenen Werte eines Zufallsexperiments vom [arithmetischen Mittel](../../../Knowledge/Mathe/Statistik/Arithmetisches%20Mittel.md).**

Die Varianz ist die quadrierte [Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md).

#### Formel

$\bar{x}$ ist das *[arithmetische Mittel](../../../Knowledge/Mathe/Statistik/Arithmetisches%20Mittel.md)*
$x_i$ ist das *Ergebnis des Zufallsexperiments*

$$
s^2 = \frac{1}{n-1} \sum\_{i=1}^n (x_i - \bar{x})^2
$$

---

[Unterschied Varianz und Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md#unterschied-empirische-varianz-varianz-und-empirische-standardabweichung-standardabweichung)

### [Empirische Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md) (Streuung)

**Die Standardabweichung misst die durchschnittliche Entfernung vom [arithmetischen Mittel](../../../Knowledge/Mathe/Statistik/Arithmetisches%20Mittel.md).**

#### Formel

$s^2$ ist die *[empirische Varianz](../../../Knowledge/Mathe/Statistik/Empirische%20Varianz.md)*
$\bar{x};$ ist das *[arithmetische Mittel](../../../Knowledge/Mathe/Statistik/Arithmetisches%20Mittel.md)*
$x_i$ ist das *Ergebnis des Zufallsexperiments*

## $$
s = \sqrt{s^2} = \sqrt{\frac{1}{n-1} \sum\_{i=1}^n (x_i - \bar{x})^2}
$$

### Unterschied [Varianz](../../../Knowledge/Mathe/Statistik/Empirische%20Varianz.md) und [Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md)

Der Unterschied zwischen dem Streuungsparameter Varianz und der Standardabweichung ist also, dass die Standardabweichung die durchschnittliche Entfernung vom Mittelwert misst und die Varianz die **quadrierte** durchschnittliche Entfernung vom Mittelwert. Andersherum gesagt, die Varianz ist die **quadrierte Standardabweichung** und die Standardabweichung ist die **Wurzel der Varianz**.

### [Variationskoeffizient](../../../Knowledge/Mathe/Statistik/Variationskoeffizient.md)

**Der Variationskoeffizient beschreibt ähnlich wie die Standardabweichung die Streuung der Daten einer Stichprobe um ihren Mittelwert.**

Gegenüber der [Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md) hat $V$ einen großen Vorteil, denn er lässt sich unabhängig von der Maßeinheit der betrachteten Stichprobe berechnen und interpretieren. Deshalb wird er auch als relatives Streuungsmaß oder **normierte Standardabweichung** bezeichnet.

Als **relatives Streuungsmaß** hängt es im Gegensatz zu den er [Varianz](../../../Knowledge/Mathe/Statistik/Empirische%20Varianz.md) und der [Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md) nicht von der Maßeinheit der statistischen Variable ab.

#### Formel

$s$ ist die *[empirische Standardabweichung](../../../Knowledge/Mathe/Statistik/Empirische%20Standardabweichung.md)*
$\bar{x}$ ist das [arithmetische Mittel](../../../Knowledge/Mathe/Statistik/Arithmetisches%20Mittel.md)
$$
V = \frac{s}{\bar{x}}   
\\text{für}   
\\bar{x} \gt 0
$$

### [Interquartilsabstand](../../../Knowledge/Mathe/Statistik/Interquartilsabstand.md)

**Sortiert man eine Stichprobe der Größe nach, so gibt der Interquartilsabstand an, wie breit da Intervall ist, in dem die mittleren 50 % der Stichprobeelemente liegen.**

Das **0,75-Quartil** entspricht dem Wert, welcher größer oder gleich 75 % aller Werte ist.
Das **0,25-Quartil** entspricht dem Wert, welcher größer oder gleich 25 % aller Werte ist.

#### Formeln

$\text{IQR} = \text{25% größter Datenpunkt} - \text{25% kleinster Datenpunkt}$

$\text{IQR} = x\_{0.75} - x\_{0.25}$

$\text{IQR} = x\_{(\[\\frac{3}{4}n\])} - x\_{(\[\\frac{1}{4}n\])}$

---

### 0.75/0.25-Quartil

$$
Q\_{0,25} = \begin{cases}
\\frac{1}{2}(x\_{n*0.25} + x\_{n*0.25+1}) \quad & \text{wenn} ; n * 0.25 ;\text{ganzzahlig} \\
x\_{\[n\*0.25\]} & \text{wenn} ; n * 0.25 ;\text{nicht ganzzahlig}
\\end{cases}
$$

### [Empirische Verteilungsfunktion](../../../Knowledge/Mathe/Statistik/Empirische%20Verteilungsfunktion.md)

**In einer empirischen Verteilungsfunktion kannst man ablesen, wie wahrscheinlich es ist, dass ein Messwert aus einer Stichprobe höchstens eine bestimmte Größe hat. Anders ausgedrückt zeigt die empirische Verteilungsfunktion also die kumulierten relativen Häufigkeiten einer Stichprobe.**

In einer empirischen Verteilungsfunktion könntest du also beispielsweise ablesen, welcher Anteil der Personen in deiner Stichprobe höchstens 35 Jahre alt ist.

#### Formel

$x_i$ ist der *Messwert*
$n_j$ ist die *absolute Häufigkeit des Messwerts $j$*  
$n\_{\text{;}}$ ist die *Gesamtanzahl der Messwerte in der Stichprobe*

$$
\\begin{align}

F_n(x_i)  & := \frac{\text{Anzahl der Beobachtungen } \le x_i}{n} \\
& = \sum\_{j=1}^{i} \frac{n_j}{n} \\
& = \frac{1}{n} \sum\_{j=1}^{n} 1\_{x_j \le x}(x_j)

\\end{align}
$$

## Geometrische Reihe

Wenn $|q| \< 1$,

dann *konvergiert* die **Geometrische Reihe**:

$$
\\sum\_{k=0}^{\infty} q^k = \frac{1}{1-q}
$$

## Wahrscheinlichkeitsrechnung

### Bei k-ten Wurf das erste Mal eine 6 oben

$$
\\Omega = {1, 2, 3, 4 ...} \\
$$
$$
P({k}) = \frac{1}{6} \Big(\frac{5}{6}\Big)^{k-1}
$$

## Anzahl ungerade

$$
B = {1, 3, 5 ...} \\
$$
$$
\\begin{align}
P(B) & = \sum\_{k \epsilon B} P({k}) \\
& = \frac{1}{6} \sum\_{k=1}^{\infty} \Big(\frac{5}{6}\Big)^{2k-1-1} \\
& = \frac{1}{6} \sum\_{k=1}^{\infty}  \Big(\frac{5}{6}\Big)^{2(k-1)} \\
& = \frac{1}{6} \sum\_{k=1}^{\infty}  \Big(\frac{25}{36}\Big)^{k-1} \\
& = \frac{1}{6} \sum\_{k=0}^{\infty}  \Big(\frac{25}{36}\Big)^{k} \Rightarrow \text{Geometrische Reihe} \\
& \Rightarrow \frac{1}{6} * \frac{1}{1-\frac{25}{36}}
\\end{align}
$$

## Kombinatorik / Anzahl der Möglichkeiten

### ✅ Zurücklegen  ✅ Reihenfolge

**Beispiel** 
Zahlenschloss, jede Ziffer kann 1-9 sein und Reihenfolge ist wichtig.

**Gleichung** 
$$
N = n^k = n * n * n \*...
$$

### ❌ Zurücklegen  ✅ Reihenfolge

**Beispiel** 
Turnier mit 15 Teams, wie viele Möglichkeiten für 1.-3. Platz?
$15 * 14 * 13 = 2730 \qquad\qquad k=3, \quad n=15$

**Gleichung**
$$
\\begin{align}
N & = n * (n-1) * (n-2) * (n-3) * ... * (n-k+1) \\
& = \frac{n!}{(n-k)!}
\\end{align}
$$

### ✅ Zurücklegen  ❌ Reihenfolge

**Beispiel** 
Urne mit farbigen Bällen.

**Gleichung**
$$
\\begin{align}
k! * N & = \frac{n!}{(n-k)!} \\
N & = \frac{n!}{k! * (n-k)!} = \binom{n}{k}
\\end{align}
$$

### ❌ Zurücklegen  ❌ Reihenfolge

**Beispiel** 
Urne mit farbigen Bällen. Bälle werden nacheinander entnommen.

**Gleichungen** 
$$
\\begin{align}
N & = \binom{n+k-1}{k} \\
& \\
& = \frac{(n+k-1)!}{k! * (n+k-1-k)!} \\
& \\
& = \frac{(n+k-1)!}{k! * (n-1)!}
\\end{align}
$$

## Rechenregeln für Wahrscheinlichkeiten

Sei Ω ein Ergebnisraum, dann gilt:

1. $0≤P(A)≤1 ;$ für $;A⊂Ω$,

1. $P(∅)=0$

1. $P(A) \le P(B)$, falls $A \subset B$ und $A,B \subset \Omega$

1. $P(A)=1−P(A)$ mit $A=\Omega \setminus A$,

1. $P(A_1 \cup A_2 \cup;...;\cup  A_k) = P(A_1) + P(A_2) + ... + P(A_k)$, 
   falls $A_1,A_2,...,A_k$ paarweise disjunkt und $A_i \subset \Omega, i=1,...,k$

1. ==$P(A \cup B)= P(A) + P(B) − P(A\cap B)$==

1. *Da $A \subset B$, ist $B = B \setminus A \cup A$, d.h.*
   $P(B) = P(B \setminus A) + P(A)$

---

### Bedingte Wahrscheinlichkeit

**Wahrscheinlichkeit A und B treffen ein**
$$
P(A \cap B) = P(A) * P_A(B)
$$

---

$$
P(A|B) = \frac{P(A \cap B)}{P(B)}
$$

**Tabelle**
![Bildschirmfoto 2022-02-06 um 20.18.53.png](../../../Attachments/Bildschirmfoto%202022-02-06%20um%2020.18.53.png)

$$
\\begin{align}
P(S \cap M) & = \frac{62}{75} 
\\
P(\bar{S} \cap M) & = \frac{13}{75} 
\\ \\
P(M \cap S) & = \frac{62}{72} 
\\
P(\bar{M} \cap S) & = \frac{10}{72} 
\\ \\
P(\bar{M} \cap \bar{S}) & = \frac{15}{28}
\\end{align}
$$

## Wahrscheinlichkeitsraum

### $\sigma$-Algebra

Eine Menge $\Lambda$ von Teilmengen von $\Omega$ heißt $\sigma$-Algebra wenn gilt:

1. $\emptyset \in 𝒜 \quad \text{und} \quad \Omega \in 𝒜$
1. $A \in 𝒜 \implies A^c := (\Omega \setminus A) \in 𝒜$
1. $A, B \in 𝒜 \implies A \cup B, ; A \cap B, ; A \setminus B \in 𝒜$
1. $A_1, ..., A_n \in 𝒜 \quad n \in \mathbb{N} \implies \quad \bigcup\_{i=1}^{n} A_n \quad \text{und} \quad \bigcap\_{i=1}^{n} A_n \in 𝒜$

**Beispiele für $\sigma$-Algebras**
Potenzmenge  𝒫($\Omega$) = Menge aller Teilmengen von $\Omega$
𝒫(${1, 2, 3}$) $= {{\emptyset}, {1}, {2}, {3}, {1, 2}, {1,3}, {2,3}, {1,2,3}}$

### Mit Zähldichten

\#todo

## Erwartungswert

**Der Erwartungswert ist der Durchschnitt, wenn ein Versuch unendlich oft durchgeführt wird.**

---

Für eine diskrete Zufallsvariable $X$, die mit WK 1 nur eine der (paarweise verschiedenen) Werte $z_1,...,z_k \in \mathbb{R}$ annimmt, ist folgendes der **Erwartungswert von X**.

$$
E\[X\] = Z_1 * P(X = Z_1) + ... + Z_n * P(X = Z_n) = \sum\_{k=1}^{\infty} Z_k * P(X = Z_k)
$$

---

Für eine stetige Zufallsvariable $X$ **mit Dichte $f$** ist der Erwartungswert von X, **falls dieser existiert**:

$$
E\[X\] = \int\_{\mathbb{R}} x * f(x)
$$

---

Sei $g$ **eine Funktion**. Dann gilt:

$$
E\[g(X)\] = \begin{cases}
\\int\_{\mathbb{R}} g(x) * f(x)
\\
\\sum\_{k} g(Z_k) * P(X = Z_k)
\\
\\end{cases}
$$

---

Sei $k \in \mathbb{N_0}$ und $g(x) = X^k$, dann ist folgendes das **k-te Moment von X**:

$$
E\[g(X)\] = E\[X^k\] - \int\_{\mathbb{R}} X^k * f(x)
$$

---

Sei $k \in \mathbb{N_0}$ und $g(x) = (x-u)^k$ und $u = E\[X\]$, dann ist folgendes das **k-te zentrale Moment von X**:

$$
E\[g(X)\] = E\[X^k\] - \int\_{\mathbb{R}} X^k f(x)
$$

---

Die **Varianz der Zufallsvariable X** ist das 2. zentrale Moment.

$$
V\[X\] = E\[(X - E\[X\])^2\]
$$

---

Der **theoretische Median** ist:

$$
F_1^{-1} \Big(\frac{1}{2}\Big)
$$

---

Seien $X, Y$ Zufallsvariablen, $f$ die Dichte von $X$ und $a,b \in \mathbb{R}$.

$X$ und $Y$ sind stochastisch unabhängig.

**Der Erwartungswert ist linear:**
$$
E\[aX + b\] = a * E\[X\] + b
$$

**Verschiebungsrate gilt:**
$$
V\[X\] = E\[X^2\] - (E\[X\])^2
$$

**Für eine lineare Transformation gilt:**
$$
V\[aX + b\] = a^2 V\[X\]
$$

**Für zwei stochastisch unabhängige Zufallsvariablen gilt:**

$$
\\begin{align}
E\[X * Y\] & = E\[X\] * E\[Y\] \\
V\[X + Y\] & = V\[X\] + V\[Y\]
\\end{align}
$$

## Wahrscheinlichkeitsmaß

$\Omega \ne \emptyset$ und 𝒜 ist $\sigma$-Algebra über $\Omega$

1. $𝑃(𝐴)∈ \[0,1\] \quad ∀ 𝐴∈𝒜$
1. $𝑃(∅)=0 \quad \mathsf{und} \quad𝑃(Ω)=1$
1. $∀𝐴∈ 𝒜 \quad \mathsf{gilt:} \quad 𝑃(𝐴^C)=1−𝑃(𝐴)$
1. $∀𝐴,𝐵∈ 𝒜 ; \mathsf{mit} ; 𝐴≤𝐵 ; \mathsf{gilt:} \quad 𝑃(𝐴)≤𝑃(𝐵)$
1. $∀𝐴,𝐵∈ 𝒜 ; \mathsf{mit} ; 𝐴∩𝐵= ∅ ; \mathsf{gilt:} \quad$ ==$𝑃(𝐴∪𝐵)=𝑃(𝐴)+𝑃(𝐵)$==

6  ![Bildschirmfoto 2022-02-03 um 21.11.59.png](../../../Attachments/Bildschirmfoto%202022-02-03%20um%2021.11.59.png)

### Laplacescher Wahrscheinlichkeitsraum

1. Nur endlich viele Elemente als mögliches Ergebnis ($\Omega$ nicht ${\infty}$)
1. Jedes der Elemente tritt mit gleicher Wahrscheinlichkeit auf

$$
P(A) = \frac{|A|}{|\Omega|}
\\quad \text{für} ; A \subseteq \Omega
$$

Damit ist $\big(\Omega, P(\Omega), P\big)$ ein Wahrscheinlichkeitsraum in dem gilt:

$$
P({\omega}) = \frac{1}{|\Omega|}
\\quad \text{für alle } ; \omega ∈ \Omega
$$

Wenn Elemente nicht-überlappen (disjunkt sind) gilt ist P auch $\sigma$-Additiv: 
$$
\\implies P\big(\bigcup\_{n=1}^{\infty} A_n\big) = \sum\_{n=1}^{\infty} P(A_n)
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
