# [Deutsch] Debian Almquist Shell (dash) trap Verwendung: Behandeln von Signalen und Exit-Status

## Overview
Der Befehl `trap` in der Debian Almquist Shell (dash) wird verwendet, um Signale und Exit-Status von Skripten zu behandeln. Mit `trap` können Sie definieren, welche Befehle ausgeführt werden sollen, wenn ein bestimmtes Signal empfangen wird oder wenn das Skript beendet wird.

## Usage
Die grundlegende Syntax des Befehls lautet:

```sh
trap [options] [commands] [signals]
```

## Common Options
- `-p`: Gibt die aktuellen `trap`-Einstellungen aus.
- `-l`: Listet alle verfügbaren Signale auf.
- `signals`: Eine Liste von Signalen, die behandelt werden sollen (z.B. `SIGINT`, `SIGTERM`).

## Common Examples

### Beispiel 1: Einfaches Signal behandeln
Um ein Skript so zu konfigurieren, dass es beim Empfang des `SIGINT`-Signals (z.B. durch Drücken von `Ctrl+C`) eine Nachricht ausgibt, können Sie Folgendes verwenden:

```sh
trap 'echo "Signal SIGINT empfangen!"' SIGINT
```

### Beispiel 2: Aufräumarbeiten bei Skriptende
Wenn Sie sicherstellen möchten, dass beim Beenden des Skripts eine Aufräumaktion durchgeführt wird, können Sie `trap` wie folgt verwenden:

```sh
trap 'echo "Aufräumarbeiten werden durchgeführt..."' EXIT
```

### Beispiel 3: Mehrere Signale behandeln
Sie können `trap` auch verwenden, um mehrere Signale zu behandeln. Zum Beispiel:

```sh
trap 'echo "Programm wurde unterbrochen!"' SIGINT SIGTERM
```

## Tips
- Verwenden Sie `trap` am Anfang Ihres Skripts, um sicherzustellen, dass alle Signale von Anfang an behandelt werden.
- Testen Sie Ihre `trap`-Befehle gründlich, um sicherzustellen, dass sie wie gewünscht funktionieren, insbesondere bei kritischen Skripten.
- Nutzen Sie die `-p`-Option, um Ihre aktuellen `trap`-Einstellungen zu überprüfen, bevor Sie Änderungen vornehmen.