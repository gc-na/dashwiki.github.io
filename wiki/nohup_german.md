# [Deutsch] Debian Almquist Shell (dash) nohup Verwendung: Prozesse im Hintergrund ausführen

## Übersicht
Der Befehl `nohup` (no hang up) wird verwendet, um Prozesse im Hintergrund auszuführen, sodass sie auch dann weiterlaufen, wenn die Sitzung beendet wird. Dies ist besonders nützlich, wenn Sie lange laufende Aufgaben haben, die nicht unterbrochen werden sollen, wenn Sie sich abmelden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
nohup [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`, `--help`: Zeigt die Hilfe für den Befehl an.
- `-v`, `--version`: Gibt die Versionsnummer des Befehls aus.
- `&`: Führt den Befehl im Hintergrund aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `nohup`:

1. **Ein einfaches Skript im Hintergrund ausführen:**
   ```bash
   nohup ./mein_skript.sh &
   ```

2. **Einen Befehl ausführen und die Ausgabe in eine Datei umleiten:**
   ```bash
   nohup ls -l > ausgabe.txt &
   ```

3. **Einen langen Download im Hintergrund durchführen:**
   ```bash
   nohup wget http://example.com/große_datei.zip &
   ```

4. **Einen Python-Server im Hintergrund starten:**
   ```bash
   nohup python3 -m http.server 8000 &
   ```

## Tipps
- Verwenden Sie `&`, um den Befehl im Hintergrund auszuführen, damit Sie die Kommandozeile weiterhin nutzen können.
- Überprüfen Sie die `nohup.out`-Datei, um die Ausgabe des Befehls zu sehen, wenn Sie keine Umleitung angegeben haben.
- Seien Sie vorsichtig mit der Verwendung von `nohup`, wenn Sie mehrere Prozesse starten, um Verwirrung bei der Ausgabe zu vermeiden.