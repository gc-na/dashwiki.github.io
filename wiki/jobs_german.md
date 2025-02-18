# [Deutsch] Debian Almquist Shell (dash) jobs Verwendung: Zeigt Hintergrundjobs an

## Übersicht
Der Befehl `jobs` in der Debian Almquist Shell (dash) wird verwendet, um eine Liste der Hintergrundjobs anzuzeigen, die in der aktuellen Shell-Sitzung laufen. Dies ist besonders nützlich, um den Status von Prozessen zu überwachen, die im Hintergrund ausgeführt werden, während der Benutzer weiterhin andere Aufgaben in der Shell ausführt.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
jobs [Optionen] [Argumente]
```

## Häufige Optionen
- `-l`: Zeigt die Prozess-ID (PID) jedes Jobs an.
- `-n`: Zeigt nur die Jobs an, die seit dem letzten Aufruf von `jobs` gestartet oder beendet wurden.
- `-p`: Gibt nur die Prozess-IDs der Jobs aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `jobs`:

1. **Einfaches Auflisten von Jobs**:
   ```bash
   jobs
   ```

2. **Auflisten von Jobs mit Prozess-IDs**:
   ```bash
   jobs -l
   ```

3. **Auflisten von neuen oder beendeten Jobs**:
   ```bash
   jobs -n
   ```

4. **Auflisten von nur den Prozess-IDs**:
   ```bash
   jobs -p
   ```

## Tipps
- Verwenden Sie `bg` oder `fg`, um einen Hintergrundjob fortzusetzen oder in den Vordergrund zu bringen, nachdem Sie ihn mit `jobs` identifiziert haben.
- Überprüfen Sie regelmäßig den Status Ihrer Hintergrundjobs, um sicherzustellen, dass sie ordnungsgemäß ausgeführt werden.
- Nutzen Sie die Optionen, um spezifische Informationen zu erhalten, die Ihnen bei der Verwaltung Ihrer Jobs helfen.