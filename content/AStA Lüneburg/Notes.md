# AStA Lüneburg – Web & Co.

## Allgemeines

Kalender im Auge behalten, manchmal erstellen Nutzer falsche Wiederholungsregeln.

Nutzer müssen dran denken, bei neuen Beiträgen die Kategorie "Allgemein" rauszunehmen.

## Finanzielles

Bei Kauf von WordPress Plugins etc, am Besten auf Rechnung bezahlen.
Ansonsten **Kostenerstattungsantrag** an Finanzreferat.

**All-Inkl Rechnung** kommt per Mail bei Webmaster-Mail an und muss an das Finanzreferat (finanz@asta-lueneburg.de) weitergeleitet werden.

## Seite – AStA-Lüneburg.de

### Staging

Im Admin Interface:

|Button|Aktion|
|------|------|
|Push changes|Staging -> Prod|
|Update|Prod -> Staging|

---

### Beschlussdatenbank

In der Beschlussdatenbank kann es vorkommen, dass XML Daten aus Microsoft Word beim kopieren in den `resolution_text` übernommen werden.
Diese XML Daten sieht der Nutzer nicht und werden vom WordPress Text Editor "verschluckt".

Diese sollten regelmäßig entfernt werden, um die Performance der Anzeige zu verbessern. Einen automatischen Check hierfür gibt es (noch?) nicht.

#### Betroffene Beschlüsse finden

Im phpMyAdmin können betroffene Beschlüsse über folgende SQL Query gefunden werden:

````sql
SELECT * FROM `wp_resolutions` WHERE `resolution_text` LIKE '%<!-- [if gte mso 9]><xml>%' ORDER BY `resolution_id` ASC;
````

Der `resolution_text` eines betroffenen Beschlusses sieht in etwa so aus:

````xml
Das Student*innenparlament beschließt, die Löhne der Mitarbeiter*innen
des Allgemeinen Student*innenausschusses vorerst auf 9,70 € 
festzulegen. Andere gefasste Beschlüsse in dieser Thematik werden 
aufgehoben.

Das Student*innenparlament befürwortet eine generelle unverzügliche 
Anpassung an die SHK-Löhne für Studierende ohne Hochschulabschluss des 
Landes Niedersachsen. Die soll erst dann geschehen, wenn der 
Haushalts- und Wirtschaftsplan dahingehend beraten wurde.

<!-- [if gte mso 9]><xml>
 <o:OfficeDocumentSettings>
  <o:RelyOnVML/>
  <o:AllowPNG/>
 </o:OfficeDocumentSettings>
</xml><![endif]--><!-- [if gte mso 9]><xml>
 <w:WordDocument>
  <w:View>Normal</w:View>
  <w:Zoom>0</w:Zoom>
  <w:TrackMoves/>
  <w:TrackFormatting/>
  <w:HyphenationZone>21</w:HyphenationZone>
  <w:PunctuationKerning/>
  <w:ValidateAgainstSchemas/>
  <w:SaveIfXMLInvalid>false</w:SaveIfXMLInvalid>
  <w:IgnoreMixedContent>false</w:IgnoreMixedContent>
  <w:AlwaysShowPlaceholderText>false</w:AlwaysShowPlaceholderText>
  <w:DoNotPromoteQF/>
  <w:LidThemeOther>DE</w:LidThemeOther>
  <w:LidThemeAsian>JA</w:LidThemeAsian>
  <w:LidThemeComplexScript>X-NONE</w:LidThemeComplexScript>

	...
	... mehr XML
	...

  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 7"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 8"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 9"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 1"/>
 
<![endif]-->
````

Einfach alles von `<!-- [if gte mso 9]><xml>` bis `<![endif]-->` entfernen.

````ad-info
Der Inhalt kann manchmal auch anderes HTML enthalten.
In dem Fall schauen, inwiefern das Sinn macht. 

*(manche sind vllt. gewollt)*
````

### Performance Improvement

Die Performance kann verbessert werden, wenn der PHP-Code, der die Tabellen anzeigt geupdated wird, sodass der Inhalt nicht mehrmals auftaucht 

Dadurch wird der fette XML Teil noch häufiger ausgegeben und vergrößert die übertragene Datenmenge immens, je nach Anzahl der Beschlüsse.

---

## Mögliche Verbesserungen

### Custom Sidebars bald deprecated

* [ ] Custom Sidebars ersetzen, wenn Gutenberg bei Widgets nicht mehr deaktivierbar ist

### Theme Funktionen -> Plugin

* [ ] Ersti Guide

---

## Bettenbörse

# Bettenbörse

\#asta #dev z

## `Announcement` Model

ID: `string`
Type: `request` | `offering`
Name: `string`
E-Mail: `string`
Phone: `string`
Gender `string` (optional)

````php
public string $id;
public string $type;
public string $name;
public string $email;
public string $phone;
public ?string $gender;

public array $availableBeds;
public int $availableBedCount;
public ?string $locationHint;
public ?string $wishes;

public \DateTime $from;
public \DateTime $until;
````

## Requests table

````sql

CREATE TABLE couchsurfing_requests (
	`id` CHAR(36) NOT NULL, 
	`type` ENUM('request','offer') NOT NULL, 
	`name` VARCHAR(128) NOT NULL, 
	`email` INT(128) NOT NULL, 
	`phone` VARCHAR(64) NOT NULL, 
	`gender` VARCHAR(128) NULL, 
	`bed_type` VARCHAR(256) NOT NULL, 
	`bed_count` SMALLINT NOT NULL DEFAULT '1',
	`location_hint` VARCHAR(1024) NULL,
	`wishes` VARCHAR(1024) NULL,
	`from` DATE NOT NULL, 
	`until` DATE NOT NULL, 
	
	PRIMARY KEY (`id`), 
	INDEX `TYPE` (`type`), 
	INDEX `FROM` (`from`), 
	INDEX `UNTIL` (`until`)
); 

````

## Database Maintenance:

Delete requests, offers and their matches if the end date is more than 2 months ago.

 > 
 > Matches will be deleted automatically due to cascading foreign keys (`DELETE CASCADE` during table creation).

````sql
DELETE FROM requests WHERE until < (NOW - 2 months)
````
