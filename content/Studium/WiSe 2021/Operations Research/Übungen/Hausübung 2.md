# Aufgaben

[UEbung2.pdf](../../../../Attachments/UEbung2.pdf)

# Finale Lösung

# Aufgabe 3

## Standardform bilden

### Schritt 0

$$
\\begin{align}
min \hspace{1cm}

& -8x_1 - 4x_2 - 2x_3 \newline

s.t. \hspace{1cm} 
& 5x_2 \le 20 \newline
& x_1 - x_3 \le 20 \newline
& 4x_1 - 8x_2 + 16x_3 \le 40 \newline
& 8x_1 - 18x_2 - 2x_3 \le 84 \newline
& x_1, x_2, x_3 \ge 0 \newline

\\end{align}
$$

### Schritt 1 *Freie Variablen* (*$x_3$*)\_ *mit* $x_3^+ - x_3^-$ *ersetzen*

nix

### Schritt 2 Gleichung $\Rightarrow$ Ungleichung

nix

### Schritt 3 $\ge$ *->* $\le$

nix

### Schritt 4 $min$ *zu* $max$

$max \hspace{1cm} 8x_1 + 4x_2 + 2x_3$

### Schritt 5

$$ 
\\begin{align} 
max \hspace{1cm} 
& 8x_1 + 4x_2 + 2x_3 \newline 

s.t. \hspace{1cm} 

& 5x_2 + x_4 = 20 \newline 
& x_1 - x_3 + x_5 = 20 \newline 
& 4x_1 - 8x_2 + 16x_3 + x_6 = 40 \newline 
& 8x_1 - 18x_2 - 2x_3 + x_7 = 84 \newline 
& x_1, x_2, x_3, x_4, x_5, x_6, x_7 \ge 0 
\\end{align}
$$

## Lösungsversuch mit Simplex Phase $\mathrm{II}$

$$ 
\\begin{align} 
max \hspace{1cm} 
& 8x_1 + 4x_2 + 2x_3 \newline 

s.t. \hspace{1cm} 

& x_4 = 20 - 5x_2 \newline 
& x_5 = 20 - x_1 - x_3 \newline 
& x_6 = 40 - 4x_1 - 8x_2 + 16x_3 \newline 
& x_7 = 84 - 8x_1 - 18x_2 - 2x_3 \newline 
& x_1, x_2, x_3, x_4, x_5, x_6, x_7 \ge 0 
\\end{align}
$$

---

$$ 
\\begin{align} 
max \hspace{1cm} 
& 320 + 4x_2 + 2x_3 - 8x_6 \newline 

s.t. \hspace{1cm} 

& x_4 = 20 - 5x_2 \newline 
& x_5 = 20 - x_3 + x_6 \newline 
& x_1 = 10 - 2x_2 + 4x_3 + \frac{x_6}{4} \newline 
& x_7 = 84 - 18x_2 - 2x_3 + 8x_6 \newline 
& x_1, x_2, x_3, x_4, x_5, x_6, x_7 \ge 0 
\\end{align}
$$

---

$$ 
\\begin{align} 
max \hspace{1cm} 
& 338.\overline{6} + 2x_3 - 8x_6 - 4x_7 \newline 

s.t. \hspace{1cm} 

& x_4 = 20 + 5x_7 \newline 
& x_5 = 20 - x_3 + x_6 \newline 
& x_1 = 10 + 4x_3 + \frac{x_6}{4} +2x_7 \newline 
& x_2 = 4.\overline{6} - \frac{x_3}{9} + \frac{8x_6}{18} + \frac{x_7}{18} \newline 
& x_1, x_2, x_3, x_4, x_5, x_6, x_7 \ge 0 
\\end{align}
$$

*ab hier komplett lost*
