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
