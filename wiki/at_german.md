# [Deutsch] Debian Almquist Shell (dash) bei at: Aufgaben zeitgesteuert ausführen

## Übersicht
Der `at`-Befehl wird verwendet, um einmalige Aufgaben zu einem bestimmten Zeitpunkt in der Zukunft zu planen. Er ermöglicht es Benutzern, Skripte oder Befehle zu einem festgelegten Zeitpunkt auszuführen, ohne dass sie manuell eingreifen müssen.

## Verwendung
Die grundlegende Syntax des `at`-Befehls lautet:

```bash
at [Optionen] [Zeitpunkt]
```

## Häufige Optionen
- `-f DATEI`: Führt die Befehle aus der angegebenen Datei aus.
- `-m`: Sendet eine E-Mail-Benachrichtigung, wenn der Job abgeschlossen ist.
- `-q QUEUE`: Gibt die Warteschlange an, in der der Job eingeordnet werden soll.
- `-l`: Listet alle geplanten `at`-Jobs auf.
- `-d`: Löscht einen bestimmten `at`-Job.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `at`-Befehls:

1. **Einen Befehl um 14:00 Uhr ausführen:**
   ```bash
   echo "echo 'Hallo Welt'" | at 14:00
   ```

2. **Ein Skript um 18:30 Uhr ausführen:**
   ```bash
   at 18:30 -f /pfad/zum/skript.sh
   ```

3. **Einen Job für morgen um 9:00 Uhr planen:**
   ```bash
   echo "backup.sh" | at 09:00 tomorrow
   ```

4. **Alle geplanten Jobs auflisten:**
   ```bash
   at -l
   ```

5. **Einen bestimmten Job löschen (Job-ID 5):**
   ```bash
   at -d 5
   ```

## Tipps
- Überprüfen Sie regelmäßig Ihre geplanten Jobs mit `at -l`, um sicherzustellen, dass keine unerwünschten Aufgaben geplant sind.
- Verwenden Sie die `-m`-Option, um Benachrichtigungen zu erhalten, wenn Ihre Jobs abgeschlossen sind.
- Stellen Sie sicher, dass die Zeitangaben im richtigen Format sind, um Missverständnisse zu vermeiden.