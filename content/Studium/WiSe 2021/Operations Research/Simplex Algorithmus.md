# Simplex Algorithmus

\#operationsresearch #uni

## Grundidee

* Die Simplex-Methode bewegt sich auf dem Rand eines konvexen Polyeders entlang benachbarter Ecken und sucht zielgerichtet eine optimale Ecke. 
* Die Methode basiert auf folgender Erkenntnis: falls eine optimale Lösung existiert, dann gibt es auch eine optimale Lösung, die in einer Ecke des Lösungsraumes (des Polyeders) ist. 
* Wie wird eine Ecke beschrieben? → m Basisvariablen und n Nichtbasisvariablen (die gleich 0 sind).
* Wie springt der Algorithmus von einer Ecke zur nächsten? → Basistausch: wird auch als Pivot-Schritt bezeichnet. D. h. wähle eine NBV (Pivot-Variable) und tausche sie gegen eine BV.

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 49,
	"scale": 1.5
}

````

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 50,
	"scale": 1.5
}

````

## Ablauf

1. Bringe das LP in die Standardform.
1. Starte mit einer zul ̈assigen Basislösung (evtl. Phase I ausführen).
1. Finde eine Nichtbasisvariable $x_q$, die den Zielfunktionswert  
   verbessern kann.  
   (*Bei Maximierung*: Nichtbasisvariablen mit positiven Koeffizienten.)  
   Falls es keine gibt, dann ist die aktuelle Basisl ̈osung optimal.  
   (*Bei Minimierung*: alle Koeffizienten in der Zielfunktion negativ.)
1. Bestimme den Wert für $x_q$ , der zur größtmöglichen Verbesserung  
   der Zielfunktion führt, ohne dass eine Basisvariable unzulässig wird.  
   Sei $x_p$ die erste Basisvariable, die den Wert von $x_q$ beschränkt.  
   Falls es keine solche Beschränkung für $x_q$ gibt, dann ist das Problem  
   unbeschränkt.
1. Führe einen Pivotschritt durch, bei dem $x_p$ die Basis verlässt und $x_q$  
   in die Basis eintritt. Gehe zu Schritt 3.

## Interpretation der Lösung

**Optimalität**
Die Koeffizienten aller Nichtbasisvariablen in der Zielfunktion sind negativ.

**Unbeschränktheit**
In einer Iteration kann eine ausgewählte Nichtbasisvariable beliebig weit erhöht werden, ohne dass sie an eine Grenze stößt. 
D. h. die Variablen-Koeffizienten sind in allen Restriktionen positiv.

**Degeneriertheit**
Mindestens eine der Basisvariablen besitzt einen Wert von Null.

**Ausgangsbasislösung ist unzulässig**
Die Ausgangsbasislösung enthält negative Werte →  
*Anwendung der Simplex-Phase I*.

## Am Fahrradbeispiel

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 51,
	"scale": 1.5
}

````

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 56,
	"scale": 1.5
}

````

 > 
 > Gleichung von $x_5$ nach $x_1$ umstellen und für $x_1$ einsetzen, da
 > $x_5$ in diesem Fall die "größte" Beschränkung hat.

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 57,
	"scale": 1.5
}

````

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 60,
	"scale": 1.5
}

````

 > 
 > Gleichung von $x_4$ nach $x_2$ umstellen und für $x_2$ einsetzen, da
 > $x_4$ in diesem Fall die "größte" Beschränkung hat..

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 62,
	"scale": 1.5
}

````

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 65,
	"scale": 1.5
}

````

````pdf
{
	"url": "[[03_-_LP_Standardform_und_Simplex_Phase_2_ohneLoesung.pdf]]",
	"page": 68,
	"scale": 1.5
}

````
