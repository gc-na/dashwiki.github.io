# [Deutsch] Debian Almquist Shell (dash) nice Verwendung: Prozesse mit angepasster Priorität ausführen

## Übersicht
Der Befehl `nice` wird verwendet, um die Priorität eines Prozesses zu ändern, der im Hintergrund ausgeführt wird. Dies ermöglicht es Benutzern, die CPU-Ressourcen, die ein Prozess beansprucht, zu steuern, indem sie ihm eine niedrigere oder höhere Priorität zuweisen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
nice [Optionen] [Befehl] [Argumente]
```

## Häufige Optionen
- `-n`, `--adjustment`: Legt die Prioritätsanpassung fest. Ein positiver Wert verringert die Priorität, während ein negativer Wert sie erhöht.
- `-h`, `--help`: Zeigt eine Hilfenachricht an und beendet den Befehl.
- `--version`: Gibt die Versionsnummer des Befehls aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `nice`-Befehls:

1. **Einen Prozess mit niedrigerer Priorität starten:**
   ```bash
   nice -n 10 myscript.sh
   ```
   In diesem Beispiel wird das Skript `myscript.sh` mit einer um 10 verringerten Priorität gestartet.

2. **Einen Prozess mit höherer Priorität starten:**
   ```bash
   nice -n -5 myscript.sh
   ```
   Hier wird das Skript `myscript.sh` mit einer um 5 erhöhten Priorität gestartet.

3. **Die aktuelle Priorität eines Prozesses anzeigen:**
   ```bash
   ps -o pid,ni,cmd
   ```
   Dieser Befehl zeigt die Prozess-ID, die nice-Werte und den Befehl der laufenden Prozesse an.

4. **Einen Befehl im Hintergrund mit niedrigerer Priorität ausführen:**
   ```bash
   nice -n 15 long_running_command &
   ```
   In diesem Beispiel wird `long_running_command` im Hintergrund mit einer um 15 verringerten Priorität ausgeführt.

## Tipps
- Verwenden Sie `nice`, um sicherzustellen, dass ressourcenintensive Prozesse die Systemleistung nicht beeinträchtigen.
- Seien Sie vorsichtig mit negativen Prioritätswerten, da sie die Systemreaktion negativ beeinflussen können, wenn sie zu hoch gesetzt werden.
- Überwachen Sie die Systemlast mit `top` oder `htop`, um die Auswirkungen von `nice` auf die Leistung zu beobachten.