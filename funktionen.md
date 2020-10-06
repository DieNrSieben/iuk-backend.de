---
layout: default
permalink: /funktionen
---
# Funktionen

> Ganz viel Text... Wenn Ihr interesse habt einfach Downloaden und ohne installation starten.

## Einsätze
//todo beschreibung was ein Einsatz ist

## Objekte
Ein Objekt kann eine Einheit, Fahrzeug oder Einrichtung sein, welche in der Software verwendert werde kann.
Ein Objekt hat folgende Eigenschaften:
- Funkrufname (OPTA)
- Alias OPTA (z.B. Wenn ein Fahrzeug HRT von einer Führungskraft verwendet wird)
- ISSI
- Icon
- Kategorie


## Einsatztagebuch
Ein Einsatztagebuch pro Einsatz  
Ein ETB Eintrag kann einem anderen ETB Eintrag angehangen werden.  
ETB Einträge haben folgenden Eigenschaften:  
Empfänger  
Melder  
Meldung   
Priorität  
Eintragender User  
Übergeordneter Eintrag  
Zeit des Eintragens  

## Patientenverwaltung
Patienten können innerhalb eines Einsatzes verwaltet werden.  
Ein Patient hat folgende (in der Software dargestellte) Eigenschaften:  
- Patientennummer  
- Vorname  
- Nachname  
- Geschlecht  
- Geburtsdatum  
- Sichtungskategorie  
- Verdachtsdiagnose  
- Bemerkung  
- Checkbox ob das Patietenprotokoll vorhanden ist  
- Zuordnung von Objekten (Zeitpunk von sowie bis)  
- Wenn transport:  
Krankenhaus  
Einsatznummer (z.B. von der Leitstelle etc.)  
Übergabezeit ans Krankenhaus  

Für mache Aktionen werden ETB Einträge erstellt:
- Anlegen von Patienten
- Entlassen von Patienten
- Abbrechen von Anfahrt/Ausrücken
- Bei ändern von Transport parametern (z.B. Krankenhaus/Einsatznummer/Übergabezeit)
- Zuordnung von Einheiten
- Entfernen von Einheiten

## Bereitstellungsraum
Ein Einsatz kann mehrere Bereitstellungsräume haben
Ein Bereitstellungsraum hat folgende Eigenschaften:
- Name

Objekte in einem Bereitstellungsraum haben folgende Eigenschaften
- Status  
1 Eintreffen erwartet  
2 Eingetroffen  
3 Ausfahrt beauftragt  
4 Ausgefahren  
5 anfahrt abgebrochen  
- Eintreffzeit
- Ausfahrtzeit
- Stärke
- Bemerkung
- Standort
- Kennzeichen
- Ansprechpartner
- Erreichbarkeit

Ein Objekt kann einem Bereitstellungsraum mehrfach zugeordnet werden (z.B. für Fahrzeuge im Pendelverkehr)



## Lagekarte
Auf der Lagekarte werden Objekte dargestellt. Icons müssen über die Objekte verwaltung bearbeitet werden.  
Objekte können entweder von Hand auf der Karte Positionniert werden oder über die Auswertung von (Tetra) LIPs automatisch positioniert werden.  
Objekte können anhand der Kategorie ein oder ausgeblendet werden.  
Die Status* von Objekten werden auf der Lagekarte visuell dargestellt und können direkt auf der Lagekarte von Hand gesetzt werden.  
Bilder können auf der Karte positioniert werden.  



## Tetra
Tetra Funkgeräte kommunizieren über ein seperates Programm mit dem Server. Dies hat den Vorteil, dass der Server nicht zwindend in der Nähe eines Funkgerätes betrieben werden muss.  
Funkgeräte können über verschiedene Schnittstellen angebunden werden (aktuell Lardis und RS232 PEI. Weitere gerne auf Anfrage)  
Auswertung und Visualisierung von 
- Status
- LIPs
- SDS Nachrichten
- Gesprächsdaten (Wer hat gerade gesprochen)



