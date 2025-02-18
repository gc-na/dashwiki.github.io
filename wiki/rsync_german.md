# [Deutsch] Debian Almquist Shell (dash) rsync Verwendung: Dateien synchronisieren

## Übersicht
Der `rsync`-Befehl ist ein leistungsfähiges Tool zur Dateiübertragung und -synchronisation. Es ermöglicht das effiziente Kopieren und Synchronisieren von Dateien und Verzeichnissen zwischen verschiedenen Speicherorten, sowohl lokal als auch über das Netzwerk.

## Verwendung
Die grundlegende Syntax des `rsync`-Befehls lautet:

```bash
rsync [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-a`: Archivmodus; kopiert Dateien rekursiv und bewahrt die meisten Attribute.
- `-v`: Verbose; zeigt detaillierte Informationen über den Fortschritt der Übertragung an.
- `-z`: Komprimiert die Daten während der Übertragung, um Bandbreite zu sparen.
- `-r`: Rekursiv; kopiert Verzeichnisse und deren Inhalte.
- `--delete`: Löscht Dateien im Zielverzeichnis, die nicht im Quellverzeichnis vorhanden sind.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `rsync`:

1. **Lokale Dateiübertragung:**
   ```bash
   rsync -av /pfad/zur/quelle /pfad/zum/ziel
   ```

2. **Übertragung zu einem Remote-Server:**
   ```bash
   rsync -av /pfad/zur/quelle benutzer@server:/pfad/zum/ziel
   ```

3. **Synchronisation eines Verzeichnisses mit Löschung:**
   ```bash
   rsync -av --delete /pfad/zur/quelle /pfad/zum/ziel
   ```

4. **Komprimierte Übertragung über das Netzwerk:**
   ```bash
   rsync -avz /pfad/zur/quelle benutzer@server:/pfad/zum/ziel
   ```

## Tipps
- Verwenden Sie den `-n`-Schalter (Trockenlauf), um zu sehen, welche Änderungen vorgenommen werden, ohne tatsächlich Daten zu übertragen:
  ```bash
  rsync -avn /pfad/zur/quelle /pfad/zum/ziel
  ```
- Achten Sie darauf, die richtigen Berechtigungen für die Quell- und Zielverzeichnisse zu haben, um Übertragungsfehler zu vermeiden.
- Nutzen Sie `rsync` regelmäßig für Backups, um sicherzustellen, dass Ihre Daten aktuell und sicher sind.