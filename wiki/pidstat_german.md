# [Deutsch] Debian Almquist Shell (dash) pidstat Verwendung: Überwachung von Prozessstatistiken

## Übersicht
Der Befehl `pidstat` wird verwendet, um verschiedene Statistiken über laufende Prozesse in einem Linux-System anzuzeigen. Er bietet Informationen wie CPU-Auslastung, Speicherverbrauch und andere wichtige Leistungskennzahlen, die für die Überwachung und Analyse von Prozessen nützlich sind.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
pidstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Zeigt die Ausgabe in einem menschenlesbaren Format an.
- `-r`: Zeigt die Speichernutzung der Prozesse an.
- `-u`: Zeigt die CPU-Nutzung der Prozesse an.
- `-p <PID>`: Überwacht einen spezifischen Prozess anhand seiner Prozess-ID.
- `-t`: Zeigt die Statistiken für Threads an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `pidstat`:

1. **CPU-Nutzung aller Prozesse anzeigen:**
   ```bash
   pidstat -u
   ```

2. **Speichernutzung eines spezifischen Prozesses überwachen:**
   ```bash
   pidstat -r -p 1234
   ```

3. **Statistiken für alle Prozesse alle 2 Sekunden anzeigen:**
   ```bash
   pidstat 2
   ```

4. **CPU- und Speichernutzung für Threads anzeigen:**
   ```bash
   pidstat -u -r -t
   ```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, insbesondere bei großen Datenmengen.
- Kombinieren Sie `pidstat` mit anderen Befehlen wie `grep`, um gezielt nach bestimmten Prozessen zu suchen.
- Nutzen Sie die Möglichkeit, die Ausgabe in eine Datei umzuleiten, um die Daten später zu analysieren:
  ```bash
  pidstat -u 2 > pidstat_output.txt
  ```