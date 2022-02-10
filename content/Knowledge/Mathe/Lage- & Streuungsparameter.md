---
cssclass: clean-embeds
---

### [Arithmetisches Mittel](Statistik/Arithmetisches%20Mittel.md)

Das **arithmetische Mittel** (auch „Mittelwert“ genannt) ist eine Kennzahl, die dir angibt, wie hoch oder niedrig **die Messwerte im Durchschnitt** sind. Für die Berechnung des arithmetischen Mittels muss man einfach alle Messwerte aufaddieren und das Ergebnis durch die Anzahl der Messwerte teilen.

#### Formel

$$
\\bar{x} = \frac{1}{n} \sum\_{i=1}^{n} x_i
$$

### [Median](Statistik/Median.md)

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

### [Empirische Spannbreite (Varianzbreite)](Statistik/Empirische%20Spannbreite%20%28Varianzbreite%29.md)

**Die emirische Spannbreite ist die Differenz zwischen dem größten und dem kleinsten Messwert.**

Da die Spannweite nur aus den zwei Extremwerten berechnet wird, ist sie nicht robust gegenüber Ausreißern.

#### Formel

$x\_{max}$ ist der *größte Messwert*
$x\_{min}$ ist der *kleinste Messwert*
–
$$
r = x\_{\text{max}} - x\_{\text{min}} = x\_{n} - x\_{1}
$$

### [Empirische Varianz](Statistik/Empirische%20Varianz.md)

**Die empirische Varianz berechnet die mittlere quadratische Abweichung der gemessenen Werte eines Zufallsexperiments vom [arithmetischen Mittel](Statistik/Arithmetisches%20Mittel.md).**

Die Varianz ist die quadrierte [Standardabweichung](Statistik/Empirische%20Standardabweichung.md).

#### Formel

$\bar{x}$ ist das *[arithmetische Mittel](Statistik/Arithmetisches%20Mittel.md)*
$x_i$ ist das *Ergebnis des Zufallsexperiments*

$$
s^2 = \frac{1}{n-1} \sum\_{i=1}^n (x_i - \bar{x})^2
$$

---

[Unterschied Varianz und Standardabweichung](Statistik/Empirische%20Standardabweichung.md#unterschied-empirische-varianz-varianz-und-empirische-standardabweichung-standardabweichung)

### [Empirische Standardabweichung](Statistik/Empirische%20Standardabweichung.md) (Streuung)

**Die Standardabweichung misst die durchschnittliche Entfernung vom [arithmetischen Mittel](Statistik/Arithmetisches%20Mittel.md).**

#### Formel

$s^2$ ist die *[empirische Varianz](Statistik/Empirische%20Varianz.md)*
$\bar{x};$ ist das *[arithmetische Mittel](Statistik/Arithmetisches%20Mittel.md)*
$x_i$ ist das *Ergebnis des Zufallsexperiments*

## $$
s = \sqrt{s^2} = \sqrt{\frac{1}{n-1} \sum\_{i=1}^n (x_i - \bar{x})^2}
$$

### Unterschied [Varianz](Statistik/Empirische%20Varianz.md) und [Standardabweichung](Statistik/Empirische%20Standardabweichung.md)

Der Unterschied zwischen dem Streuungsparameter Varianz und der Standardabweichung ist also, dass die Standardabweichung die durchschnittliche Entfernung vom Mittelwert misst und die Varianz die **quadrierte** durchschnittliche Entfernung vom Mittelwert. Andersherum gesagt, die Varianz ist die **quadrierte Standardabweichung** und die Standardabweichung ist die **Wurzel der Varianz**.

### [Variationskoeffizient](Statistik/Variationskoeffizient.md)

**Der Variationskoeffizient beschreibt ähnlich wie die Standardabweichung die Streuung der Daten einer Stichprobe um ihren Mittelwert.**

Gegenüber der [Standardabweichung](Statistik/Empirische%20Standardabweichung.md) hat $V$ einen großen Vorteil, denn er lässt sich unabhängig von der Maßeinheit der betrachteten Stichprobe berechnen und interpretieren. Deshalb wird er auch als relatives Streuungsmaß oder **normierte Standardabweichung** bezeichnet.

Als **relatives Streuungsmaß** hängt es im Gegensatz zu den er [Varianz](Statistik/Empirische%20Varianz.md) und der [Standardabweichung](Statistik/Empirische%20Standardabweichung.md) nicht von der Maßeinheit der statistischen Variable ab.

#### Formel

$s$ ist die *[empirische Standardabweichung](Statistik/Empirische%20Standardabweichung.md)*
$\bar{x}$ ist das [arithmetische Mittel](Statistik/Arithmetisches%20Mittel.md)
$$
V = \frac{s}{\bar{x}}   
\\text{für}   
\\bar{x} \gt 0
$$

### [Interquartilsabstand](Statistik/Interquartilsabstand.md)

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

### [Empirische Verteilungsfunktion](Statistik/Empirische%20Verteilungsfunktion.md)

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
