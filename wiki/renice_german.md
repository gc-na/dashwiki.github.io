# [Deutsch] Debian Almquist Shell (dash) renice Verwendung: Ändern der Priorität von Prozessen

## Übersicht
Der Befehl `renice` wird verwendet, um die Priorität von laufenden Prozessen in einem Unix-ähnlichen Betriebssystem zu ändern. Mit `renice` können Sie die CPU-Zuteilung für Prozesse anpassen, was nützlich ist, um die Systemleistung zu optimieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
renice [Optionen] [Wert] [PID...]
```

Hierbei steht `[Wert]` für die neue Priorität, die Sie den Prozessen zuweisen möchten, und `[PID...]` für die Prozess-IDs der zu ändernden Prozesse.

## Häufige Optionen
- `-n`: Gibt den neuen Prioritätswert an.
- `-p`: Gibt an, dass die folgenden Argumente Prozess-IDs sind.
- `-g`: Ändert die Priorität aller Prozesse einer bestimmten Gruppe.
- `-u`: Ändert die Priorität aller Prozesse eines bestimmten Benutzers.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `renice`:

1. Ändern der Priorität eines Prozesses mit der PID 1234 auf 10:

   ```bash
   renice -n 10 -p 1234
   ```

2. Ändern der Priorität mehrerer Prozesse (PIDs 1234 und 5678) auf 5:

   ```bash
   renice -n 5 -p 1234 5678
   ```

3. Ändern der Priorität aller Prozesse eines bestimmten Benutzers (z.B. "benutzername") auf 15:

   ```bash
   renice -n 15 -u benutzername
   ```

4. Ändern der Priorität aller Prozesse einer bestimmten Gruppe (z.B. Gruppe 1000) auf 0:

   ```bash
   renice -n 0 -g 1000
   ```

## Tipps
- Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen verfügen, um die Priorität von Prozessen zu ändern. Einige Änderungen erfordern Root-Rechte.
- Verwenden Sie `top` oder `ps`, um die aktuellen Prozess-IDs und deren Prioritäten zu überprüfen, bevor Sie `renice` verwenden.
- Seien Sie vorsichtig beim Erhöhen der Priorität von Prozessen, da dies die Systemleistung negativ beeinflussen kann, wenn zu viele Prozesse hohe Prioritäten haben.