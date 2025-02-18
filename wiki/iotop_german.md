# [Deutsch] Debian Almquist Shell (dash) iotop Verwendung: Überwachen der Festplatten-E/A-Aktivität

## Übersicht
Der Befehl `iotop` wird verwendet, um die Echtzeit-Festplatten-E/A-Aktivität von Prozessen auf einem Linux-System zu überwachen. Er zeigt an, welche Prozesse die meiste Ein- und Ausgabe (E/A) durchführen, was bei der Diagnose von Leistungsproblemen hilfreich sein kann.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
iotop [Optionen] [Argumente]
```

## Häufige Optionen
- `-o`, `--only`: Zeigt nur Prozesse an, die aktuell E/A durchführen.
- `-b`, `--batch`: Führt `iotop` im Batch-Modus aus, nützlich für die Ausgabe in Dateien.
- `-d`, `--delay`: Setzt die Zeitverzögerung (in Sekunden) zwischen den Aktualisierungen.
- `-p`, `--pid`: Überwacht nur die angegebenen Prozess-IDs.

## Häufige Beispiele
1. **Echtzeitüberwachung der E/A-Aktivität:**
   ```bash
   iotop
   ```

2. **Nur Prozesse mit E/A-Aktivität anzeigen:**
   ```bash
   iotop -o
   ```

3. **Ausgabe im Batch-Modus alle 5 Sekunden:**
   ```bash
   iotop -b -d 5
   ```

4. **Überwachung eines bestimmten Prozesses (z.B. PID 1234):**
   ```bash
   iotop -p 1234
   ```

## Tipps
- Verwenden Sie den Batch-Modus, wenn Sie die Ausgabe in eine Datei umleiten möchten, um die E/A-Aktivität über einen längeren Zeitraum zu protokollieren.
- Kombinieren Sie `iotop` mit anderen Befehlen wie `grep`, um gezielt nach bestimmten Prozessen zu suchen.
- Achten Sie darauf, `iotop` mit Root-Rechten auszuführen, um vollständige Informationen über alle Prozesse zu erhalten.