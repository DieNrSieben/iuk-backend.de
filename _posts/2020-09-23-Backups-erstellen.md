---
layout: post
title: "Erstellen von Backups"
categories: blog
---

Der erstellen von Backups ist oft ein leidiges Thema welches sich in IuK gruppen (vor allem wenn diese durch ehrenamtliche Kräfte unterhalten werden) keiner sonderlich hohen beliebtheit erfreut.

Aus diesem Grund haben wir versucht die Hürden hierfür möglichst klein zu halten.

Um den zentralen Server zu sichern muss lediglich die Serveranwendung gestoppt werden und anschließend kann der Order `uploads`, die Dateien `config.json` sowie `app.db` (wenn vorhanden auch die `app.db-shm` und `app.db-wal` dateien) weggesichert werden.
Um Speicherplatz zu sparen muss der Order `uploads/osm` nicht mit gesichert werden, da sich in diesem Ordner nur die zwischengesicherten Hintergründe der Lagekarte befinden. 

Unter Linux lassen sich die Dateien in eine Zip-Datei mit dem folgenden Befehl packen
```bash
zip -9 -r "backup-iuk-backend-server-$(date +"%Y-%m-%d_%H-%M").zip" app.db* config.json uploads/ -x "uploads/osm/*"
```