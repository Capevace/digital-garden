**Der Wert, der genau in der Mitte einer Datenverteilung liegt, nennt sich Median oder Zentralwert.**

#### Formel
**Reelle Zahlen (Integer):**
$$
\tilde{x}= \begin{cases}
    \frac{1}{2} (x_{(\frac{n}{2})} + x_{(\frac{n}{2} + 1)}) & \text{falls gerade} \\
    x_{\frac{n+1}{2}} & \text{falls ungerade} \\
  \end{cases}
$$

**Nicht reelle Zahlen (Float):**
$$
\tilde{x} = x_{([\frac{n}{2}])}
$$

$[\text{ | }] = \text{Aufrundungsfunktion}$ 


### Aufgaben-Beispiel

 Berechnen Sie den theoretischen Median:

$F (median) = 0.5 \implies median = F^{−1}(0.5)$. 

Wegen dem in 35.iv blau markierten Teil gilt 
$median = F^{−1}(0.5) = 2$.