## Aufgabe 2

![[Screenshot 2021-11-12 at 12.20.55.png]]

$max = 50000 * x_G + 70000 * x_T + 190000 * x_C$

**Fläche**
$800 * x_G + 1100 * x_T + 3000 * x_C \le 65000$

**Grünfutter**
$1.5 * x_G + 14 * x_T \le 420$

**Fleisch**
$8 * x_C \le 60$

**Pflegekräfte**
$0.5 * x_G + 2 * x_T + 2 * x_C \le 55$

**Sicherheitskräfte**
$0.25 * x_G + 2 * x_T + 10 * x_C \le 80$

**Wissenschaftler**
$x_G + 3 * x_T + 2 * x_C \le 60$

**Herdenbedingungen**
$x_G \le 15 * y_G$
$x_T \le 6  * y_T$

## Lingo

```lingo
MAX = 50000 * xg + 70000 * xt + 190000 * xc

800 * xg + 1100 * xt + 3000 * xc <= 65000
1.5 * xg + 14 * xt <= 420
8 * xc <= 60
0.5 * xg + 2 * xt + 2 * xc <= 55
0.25 * xg + 2 * xt + 10 * xc <= 80
xg + 3 * xt + 2 * xc <= 60
xg <= 15 * yg
xt <= 6  * yt

@BIN(yg)
@BIN(yt)

END
```