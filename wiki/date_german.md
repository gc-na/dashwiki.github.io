# [Deutsch] Debian Almquist Shell (dash) date: Datum und Uhrzeit anzeigen

## Übersicht
Der Befehl `date` wird verwendet, um das aktuelle Datum und die Uhrzeit anzuzeigen oder um das Datum in einem bestimmten Format auszugeben. Er ist ein nützliches Werkzeug, um zeitbezogene Informationen in Skripten oder auf der Kommandozeile zu erhalten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
date [Optionen] [Argumente]
```

## Häufige Optionen
- `+FORMAT`: Gibt das Datum in einem benutzerdefinierten Format aus.
- `-u`: Zeigt die UTC-Zeit (Koordinierte Weltzeit) an.
- `-d STRING`: Gibt das Datum an, das durch den angegebenen String beschrieben wird.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des Befehls `date`:

1. Aktuelles Datum und Uhrzeit anzeigen:
   ```bash
   date
   ```

2. Datum im Format "Tag-Monat-Jahr" anzeigen:
   ```bash
   date +"%d-%m-%Y"
   ```

3. UTC-Zeit anzeigen:
   ```bash
   date -u
   ```

4. Ein bestimmtes Datum anzeigen, z.B. den 1. Januar 2023:
   ```bash
   date -d "2023-01-01"
   ```

5. Datum und Uhrzeit in einer benutzerdefinierten Form anzeigen:
   ```bash
   date +"%A, %d. %B %Y %H:%M:%S"
   ```

## Tipps
- Nutzen Sie die Formatoption `+FORMAT`, um das Datum genau nach Ihren Bedürfnissen anzupassen.
- Verwenden Sie die `-u` Option, wenn Sie mit internationalen Zeitangaben arbeiten, um Verwirrung durch Zeitzonen zu vermeiden.
- Experimentieren Sie mit verschiedenen Formatzeichen, um das Datum in der gewünschten Form darzustellen.