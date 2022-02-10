# Vorgehen vor Ort

## Genereller Ablauf

1. Analysieren, wo Daten gespeichert sein könnten
   * Cloud? etc.
1. Analysieren welche Daten Beweismittel sein könnten
   * ggf. Triage
   * Entscheidung treffen, System ins Labor mitzunehmen oder vor Ort zu sichern
   * Im Zweifelsfall zu viel sichern, als zu wenig
1. Ermitteln der Sicherungsreihenfolge
   * Was dauert am längsten?
   * Womit sollte ich anfangen?
1. Veränderungen am System erschweren
   * z.B. Netzwerkzugriffe unterbinden
1. Datensicherung durchführen
1. Systemzeit und ggf. Zeitabweichung zur Referenzzeit erfassen
1. Dokumentation
   * Jeder Schritt
   * Anwesende Personen

## Sicherungsreihenfolge

1. CPU Register, Cache
1. Routing Tabellen, ARP Cache, Prozessliste, Netzstatus, Kerneldaten, RAM Inhalt
1. Tempotäte Dateisysteme, Auslagerungsdateien
1. Inhalte von Festplatten
1. Logging- und Monitoring-Daten (teils auf anderen Systemen)
1. Physiche Konfigurationen, Netzwerktopologien
1. Backups, archivierte Daten

## Vor Ort zu beachten

* Meiste unumkerhbare Fehler passieren hier!
* Integrität ermöglichen (Prüfsummen / Signaturen erzeugen)
* Datenschutz beachten
* Anerkannte Tools verwenden
* **Das Vorgehen vor Ort ist die Grundlage für den Erfolg der Untersuchung**
