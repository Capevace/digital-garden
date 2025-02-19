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
