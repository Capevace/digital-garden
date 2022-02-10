# Modellierung

\#operationsresearch #uni
19.10.21

## Fallbeispiel Fahrradfabrik

* Wir betrachten eine Fahrradfabrik, in der unterschiedliche Fahrradtypen (Normal und Deluxe) hergestellt werden.
* Für jeden Typ besteht wegen begrenzter Materialzufuhr eine maximale Fertigungszahl.
* Die Fahrradtypen werden auf gemeinsam genutzten Maschinen gefertigt, die eine maximale Laufzeit haben.
* Gesucht ist die gewinnmaximale Kombination der Typen, die in Fertigung gehen sollen.

### Problem

* Entscheidungssituation: Wie viele Produkte der Sorten Normal und Deluxe sollen gefertigt werden, wenn der Gewinn maximal sein soll?
  * 2 Entscheidungen (Anzahl der Sorten Normal und Deluxe)
* Jede Teilentscheidung beeinflusst das Ergebnis
  * Auswirkungen von Teilentscheidungen sind nicht unmittelbar erkennbar
    * höhere Anzahl von Deluxe-Produkten könnte eine geringere Fertigung bei Normal-Produkten erzwingen
* Die Greedy-Strategie funktioniert nicht
  * Maschinenlaufzeit-abhängig (Mehr Gewinn mit Deluxe, dauert aber länger)

## Grundmodell

**1.** Zielfunktion: Eine Größe soll maximiert oder minimiert werden (oft Gewinn oder Kosten)

**2.** Entscheidungsvariablen: Für das Ziel relevante Größen, die wir beeinflussen können

**3.** Restriktionen: Die Einflussgrößen können nicht beliebig gewählt werden

## Am Beispiel

### 2D Betrachtung

* Der Gewinn pro Fahrrad liegt bei 90 Euro bzw. 120 Euro
* Maximalproduktion pro Typ betr ̈agt 700 und 400 Stück
* Maschinenlaufzeit beschränkt die Gesamtzahl auf 800 Stück
* Fertigung von einem Deluxe Fahrrad dauert 12 Min und damit doppelt so lange wie ein Normales. 
* Insgesamt stehen 100 Arbeitsstunden pro Tag zur Verfügung

### Am Modell

**1.** Zielfunktion

$\max  z = 120x1 + 90x2$
Entscheidungsvariablen mit Koeffizienten, hier Gewinn

**2.** Entscheidungsvariablen

$x1$ = Anzahl der herzustellenden Fahrräder des Typs Deluxe 
$x2$ = Anzahl der herzustellenden Fahrräder des Typs Normal

**3.** Restriktionen

Produktionsmaximum für beide:
$x1 + x2 \<= 800$ 

Typen: 800 

Zeitrestriktion?

Keine negative Produktion
$x1 >= 0, x2 >= 0$

### Mathematisches Modell

Zielfunktion (Gewinnmax.):
$\max z = 120x1 + 90x2$

subject to (s.t.)

\| Rechnung                | Bedeutung                     |   |
\| ----------------------- | ----------------------------- | --- | --- |
\| $x1 + x2 	\<= 800$       | Restriktion(Produktionsmenge) |     |     |
\| $x1 \<= 400$             | Restriktion(Maximum normal)   |     |     |
\| $x2 \<= 700$             | Restriktion(Maximum deluxe)   |     |     |
\| $12x1 + 6x2 \<= 6000$    | Restriktion(Zeit)             |     |     |
\| $x1, x2 >= 0$           | Restriktion(Nichtnegativität) |     |     |

````ad-warning
title: In der Klausur muss bei Aufgaben die Nichtnegativitäts Bedingung auftauchen!

x1, x2 >= 0

````

````pdf
{
	"url": "[[01 - Grafisches Loesen.pdf]]",
	"page": 36,
	"scale": 2
}

````

## Grafische Lösung – Vorgehen

### Schritt 1

Zeichne Restriktionsgeraden des LP-Problems mit zwei Variablen

Diese sind die Randgeraden der durch die Restriktionen dargestellten Halbebenen.  
Bestimme den zulässigen Bereich

### Schritt 2

Lösungen gleichen Wertes liegen auf sog. Isogewinn-Hyperebenen (im 2-dimensionalen Fall auf Isogewinn-Geraden).

Setze Zielfunktionswert auf eine Konstante z = z0  
zeichne die so definierte Isogewinn-Gerade.

### Schritt 3

Verschiebe Isogewinngerade parallel bis ggf. zu einer optimalen Ecke.
