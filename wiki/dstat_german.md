# [Deutsch] Debian Almquist Shell (dash) dstat Verwendung: Systemressourcen überwachen

## Übersicht
Der Befehl `dstat` ist ein vielseitiges Werkzeug zur Überwachung von Systemressourcen in Echtzeit. Es kombiniert die Funktionen mehrerer anderer Befehle wie `vmstat`, `iostat` und `netstat`, um eine umfassende Übersicht über die Leistung Ihres Systems zu bieten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
dstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-c`: Zeigt die CPU-Nutzung an.
- `-d`: Zeigt die Festplattennutzung an.
- `-n`: Zeigt die Netzwerkstatistiken an.
- `-r`: Zeigt den Speicherverbrauch an.
- `-t`: Fügt einen Zeitstempel zu den Ausgaben hinzu.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `dstat`:

1. **CPU- und Speicherstatistiken anzeigen:**
   ```bash
   dstat -c -r
   ```

2. **Festplatten- und Netzwerkstatistiken anzeigen:**
   ```bash
   dstat -d -n
   ```

3. **Alle Statistiken mit Zeitstempel anzeigen:**
   ```bash
   dstat -t -cdng
   ```

4. **Daten alle 2 Sekunden aktualisieren:**
   ```bash
   dstat 2
   ```

## Tipps
- Verwenden Sie `dstat` in Kombination mit anderen Befehlen, um detailliertere Analysen durchzuführen.
- Nutzen Sie die Option `-p`, um die Prozesse anzuzeigen, die die meisten Ressourcen verbrauchen.
- Speichern Sie die Ausgabe in eine Datei, um die Leistung über einen längeren Zeitraum zu überwachen:
  ```bash
  dstat > dstat_output.txt
  ```