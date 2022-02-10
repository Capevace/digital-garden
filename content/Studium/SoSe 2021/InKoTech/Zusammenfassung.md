# Informations- und Kommunikations-Technologien

\#sose2021

## **Ein wenig Hardware** – Prozessor

### Datenbus / Datenregister

* Transport von Daten zwischen Speicher und Prozessor
* Auch für Transport zu anderer Peripherie verwendet

### Steuerbus

* aktiviert / deaktiviert Komponenten innerhalb / außerhalb des Prozessors
* wenn per Adressbus auf eine Speicherzelle zugegriffen werden soll, so muss der Speicherzelle zusätzlich mitgeteilt werden, ob gelesen oder geschrieben werden soll

### Rechenwerk

Das Rechenwerk führt einfachste Rechenoperationen aus. Diese Operationen umfassen arithmetische Operationen, wie z.B. Additionen, oder logische Operationen, wie z.B. ein UND

### Register

* enthalten Zahlenwerte zu einzelnen Operationen
* Statusregister: enthält Flags (ZERO, CARRY, SIGN etc.)

### Steuerwerk, Befehlsdekoder & Befehlsregister

* Steuerwerk lädt Befehl in Befehlsregister und wird dann mit Tabelle decoded

### Stapel (Stack)

* Speichert momentanes Prozessorabbild im Falle von Interrupts etc.

### Cache

* Cached ergebnisse

## **Ein kleiner Rechner** – Microcontroller

### Micro-Controller

* Zusammengesetzt aus min.:
  * Prozessor
  * Speicher
  * Eingabe-Schnittstellen
  * Ausgabe-Schnittstellen

### ATMEGA328P-PU

* keinen Datenbus und auch keinen Adressbus

### Micro-Controller vs. PC-Prozessor

![Informationstechnologie .png](../../../Attachments/Informationstechnologie%20.png)

## **Pull-Up / Pull-Down Buttons**

![Screenshot 2021-07-22 at 16.26.41.png](../../../Attachments/Screenshot%202021-07-22%20at%2016.26.41.png)

### Pull-Down

![Screenshot 2021-07-22 at 16.20.59.png](../../../Attachments/Screenshot%202021-07-22%20at%2016.20.59.png)

Wenn Taster *nicht* gedrückt, zieht Widerstand an Masse PIN13 auf 0V.
Wenn Taster gedrückt, dann 5V.
Wiederstand zu niedrig um bei 5V was auszumachen.

### Pull-Up

![Screenshot 2021-07-22 at 16.23.31.png](../../../Attachments/Screenshot%202021-07-22%20at%2016.23.31.png)

Wenn *nicht* gedrückt, zieht Widderstand PIN13 auf 5V.
Wenn gedrückt dann 0V.
