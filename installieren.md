---
layout: default
permalink: /installieren
---
# Installationsanleitung
[Windows](#windows) 

[Linux](#linux)

[Mac OS](#mac-os)

## Grundsätzliches

Die Daten werde in einer Sqlite Datenbank gespeichert `app.db`. 

Sqlite hat den entscheidenen Vorteil, dass hierfür keine extra Serversoftware betrieben werden muss. Zudem ist die Datenbank einfach zu Sichern ist. Ein Nachteil von Sqlite ist, dass nur limitiert paralele schreibvorgänge möglich sind. Dies sollte aber bei der nutzung von bis zu 20 parallelen Benutzern kein Problem sein.
//Todo: Blogeintrag über Serverbackup erstellen.

Dateien werden nicht in der Sqlite Datenbank gespeichert sondern in einem Ordern mit dem namen `uploads`. Dieser Ordner hat zwei unterordner 
1. `map` in diesem werden die hintergrund bilder der Lagekarte gespeichert.
2. `osm` in diesem Ordner werden die Bilddaten der eigentlichen Karte gespeichert. Heißt die Openstreetmap Daten werden zwischengespeichert für den fall, dass die Internetverbindung abbricht. So kann zumindest mit den bereits angesehenen kartenausschnitte weitergearbeitet werden.

Ein teil der Konfiguration wir in der `config.json` datei gespeichert. Diese wird beim ersten start des Servers angelegt. Nach änderungen an der `config.json` muss der Server neugestartet werden.



<details>
    <summary>config.json</summary>
    <pre><code>{
    "port": 3000, //Port für den Webserver
    "tetraAuthKey": "123456789", //Key zum Authentifizieren der tetraClients
    "osmCacheMaxAge": "604800", //Maximales alter (in sekunden) für die gespeicherten OSM tiles
    "tetra": {
        "save_detected_optas":1, //Erstellt ein neue Objekte wenn der absender nicht bekannt ist
        "save_unknown_calls":1, //Speichert Rufinformationen von unbekannten absendern
        "save_unknown_lips":1, //Speichert LIPs von unbekannten absendern
        "save_unknown_statuses":1, // Speichert Statuse von unbekannten absendern
        "save_unknown_mails":1, //Speichert SDS Nachrichten von unbekannten absendern
        "storage_duration_calls":90, //Löscht Rufinformationen nach x Tagen
        "storage_duration_lips":999, //Löscht LIPS nach x Tagen
        "storage_duration_statuses":999, //Löscht Status Nachrichten nach x Tagen
        "storage_duration_mails":999 //Löscht SDS Nachrichten nach x Tagen
    },
    "pushover":{
        "user": "",
        "token": ""
    }
}</code></pre>
</details>



## Windows

Laden Sie die Windows Zip Datei herunter entpacken diese und starten die `iuk-backend-Server_win-x64.exe`.
Stellen Sie sicher, dass die Datei eine Freigabe in der Windows Firewall hat.
//Todo: Anleitung für Service erstellen.


## Linux
Laden Sie die Linux Zip Datei herunter entpacken diese und starten die Datei `iuk-backend-Server_linux-x64`.
//Todo: Anleitung für Service erstellen.

Wenn der Webserver auf einem Port unter 1024 laufen soll muss die Anwendung entweder mit root rechten ausgeführt werden oder mittels Capabilities die entsprechenden berechtigungen erteilt werden.
```bash
setcap 'cap_net_bind_service=+ep' /Pfad/zum/iuk-backend-Server_linux-x64
```
## Mac OS
Laden Sie die MacOS Zip Datei herunter entpacken diese und starten die Datei `iuk-backend-Server_macos-x64`.


