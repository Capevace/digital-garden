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
