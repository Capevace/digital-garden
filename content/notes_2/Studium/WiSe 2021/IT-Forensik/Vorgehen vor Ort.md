# Vorgehen vor Ort

## Genereller Ablauf
1. Analysieren, wo Daten gespeichert sein könnten
	- Cloud? etc.
2. Analysieren welche Daten Beweismittel sein könnten
	- ggf. Triage
	- Entscheidung treffen, System ins Labor mitzunehmen oder vor Ort zu sichern
	- Im Zweifelsfall zu viel sichern, als zu wenig
3. Ermitteln der Sicherungsreihenfolge
	- Was dauert am längsten?
	- Womit sollte ich anfangen?
4. Veränderungen am System erschweren
	- z.B. Netzwerkzugriffe unterbinden
5. Datensicherung durchführen
6. Systemzeit und ggf. Zeitabweichung zur Referenzzeit erfassen
7. Dokumentation
	- Jeder Schritt
	- Anwesende Personen


## Sicherungsreihenfolge
1. CPU Register, Cache
2. Routing Tabellen, ARP Cache, Prozessliste, Netzstatus, Kerneldaten, RAM Inhalt
3. Tempotäte Dateisysteme, Auslagerungsdateien
4. Inhalte von Festplatten
5. Logging- und Monitoring-Daten (teils auf anderen Systemen)
6. Physiche Konfigurationen, Netzwerktopologien
7. Backups, archivierte Daten

## Vor Ort zu beachten

- Meiste unumkerhbare Fehler passieren hier!
- Integrität ermöglichen (Prüfsummen / Signaturen erzeugen)
- Datenschutz beachten
- Anerkannte Tools verwenden
- **Das Vorgehen vor Ort ist die Grundlage für den Erfolg der Untersuchung**