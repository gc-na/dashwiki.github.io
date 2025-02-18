# [Deutsch] Debian Almquist Shell (dash) bg: Prozesse im Hintergrund ausführen

## Übersicht
Der Befehl `bg` wird in der Debian Almquist Shell (dash) verwendet, um einen angehaltenen Prozess im Hintergrund fortzusetzen. Dies ermöglicht es Benutzern, mit der Shell weiterzuarbeiten, während der Prozess weiterhin läuft.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
bg [options] [arguments]
```

## Häufige Optionen
- **%job_spec**: Gibt die Job-Spezifikation an, die im Hintergrund fortgesetzt werden soll. Dies kann eine Job-ID oder ein Job-Name sein.
- **-n**: Verhindert die Ausgabe von Job-IDs.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `bg`-Befehls:

1. **Einen angehaltenen Prozess im Hintergrund fortsetzen**:
   ```bash
   bg %1
   ```
   Dies setzt den Prozess mit der Job-ID 1 im Hintergrund fort.

2. **Einen angehaltenen Prozess ohne Job-ID fortsetzen**:
   ```bash
   bg
   ```
   Wenn nur ein Prozess angehalten wurde, wird dieser im Hintergrund fortgesetzt.

3. **Einen spezifischen Job fortsetzen**:
   ```bash
   bg %myjob
   ```
   Hier wird der Job mit dem Namen `myjob` im Hintergrund fortgesetzt.

## Tipps
- Verwenden Sie den Befehl `jobs`, um eine Liste aller laufenden und angehaltenen Prozesse anzuzeigen, bevor Sie `bg` verwenden.
- Achten Sie darauf, dass Prozesse, die im Hintergrund laufen, möglicherweise Ausgaben erzeugen, die Sie in der Konsole sehen. Nutzen Sie Umleitungen, um diese Ausgaben zu steuern.
- Wenn Sie mehrere Prozesse im Hintergrund haben, können Sie die Job-Spezifikation verwenden, um gezielt einen bestimmten Prozess fortzusetzen.