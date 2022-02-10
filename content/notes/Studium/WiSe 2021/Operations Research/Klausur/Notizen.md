# Modellieren

# Standardform
1. $min \implies max \quad$ durch $*(-1)$ 
2. $\ge \implies \le \qquad\qquad$ durch $*(-1)$
3. $= \implies \le$
	- 2 Nebenbedingungen erstellen (Bsp: $g(x) = y$)
		1. $g(x) \le y$
		2. $g(x) * (-1) \le y * (-1)$
1.  Freie Variablen (ohne Nicht-Negativität)
	1. $x_i = x_i^+ - x_i^-$

## Simplex Phase 1
1. Modell in Standardform bringen
2. Wenn BL zulässig (keine negativen Werte in der Basis), dann starte Phase 2
3. Neue Zielfunktion $s$ aufstellen, und $z = ... = 0$ in die Restriktionen
	$s= f_{x_i} +...+f_{x_j}$ für alle Basisvariablen $x_i ... x_j$ die negative Werte haben
1. Dann Simplex mit $s$ durchführen, solange es noch negative Basisvariablen gibt
2. Mit neuer $z$ in Phase 2 starten

## Simplex Phase 2
### Interpretation der Lösung

**Optimalität**
Die Koeffizienten aller Nichtbasisvariablen in der Zielfunktion sind negativ.

**Degeneriertheit**:  
Mindestens eine der Basisvariablen besitzt einen Wert von Null.

**Unbeschränktheit**
In einer Iteration kann eine ausgewählte Nichtbasisvariable beliebig weit erhöht werden, ohne dass sie an eine Grenze stößt. 
D. h. die Variablen-Koeffizienten sind in allen Restriktionen positiv.

**Ausgangsbasislösung ist unzulässig**
Die Ausgangsbasislösung enthält negative Werte.