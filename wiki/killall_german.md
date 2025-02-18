# [Deutsch] Debian Almquist Shell (dash) killall Verwendung: Prozesse beenden

## Übersicht
Der Befehl `killall` wird verwendet, um Prozesse zu beenden, die einen bestimmten Namen haben. Im Gegensatz zu `kill`, das einen Prozess anhand seiner PID (Prozess-ID) beendet, ermöglicht `killall` das Beenden aller Prozesse mit einem bestimmten Namen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
killall [Optionen] [Argumente]
```

## Häufige Optionen
- `-u <Benutzer>`: Beendet nur die Prozesse, die von dem angegebenen Benutzer gestartet wurden.
- `-i`: Fragt vor dem Beenden jedes Prozesses nach Bestätigung.
- `-q`: Unterdrückt Fehlermeldungen, wenn kein Prozess gefunden wird.
- `-s <Signal>`: Sendet ein spezifisches Signal an die Prozesse (z.B. `SIGTERM`, `SIGKILL`).

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `killall`:

1. Beenden aller Instanzen eines Prozesses namens `firefox`:
   ```bash
   killall firefox
   ```

2. Beenden aller `ssh`-Prozesse, die von einem bestimmten Benutzer gestartet wurden:
   ```bash
   killall -u benutzername ssh
   ```

3. Beenden eines Prozesses mit Bestätigungsaufforderung:
   ```bash
   killall -i firefox
   ```

4. Senden eines spezifischen Signals (z.B. `SIGKILL`) an alle `gedit`-Prozesse:
   ```bash
   killall -s SIGKILL gedit
   ```

5. Unterdrücken von Fehlermeldungen, wenn kein Prozess gefunden wird:
   ```bash
   killall -q firefox
   ```

## Tipps
- Verwenden Sie die Option `-i`, um versehentliche Beendigungen zu vermeiden, insbesondere bei kritischen Prozessen.
- Seien Sie vorsichtig mit `killall`, da es alle Prozesse mit dem angegebenen Namen beendet, was zu Datenverlust führen kann, wenn nicht gespeicherte Arbeiten vorhanden sind.
- Überprüfen Sie mit `pgrep <prozessname>`, welche Prozesse aktiv sind, bevor Sie `killall` verwenden, um sicherzustellen, dass Sie die richtigen Prozesse beenden.