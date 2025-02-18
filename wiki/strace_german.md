# [Deutsch] Debian Almquist Shell (dash) strace Verwendung: Systemaufrufe verfolgen

## Übersicht
Der Befehl `strace` wird verwendet, um Systemaufrufe und Signale eines Programms zu verfolgen. Dies ist besonders nützlich für die Fehlersuche und das Debugging, da es Einblicke in die Interaktionen eines Programms mit dem Betriebssystem bietet.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
strace [Optionen] [Argumente]
```

## Häufige Optionen
- `-e trace=all`: Verfolgt alle Systemaufrufe.
- `-p <PID>`: Verfolgt ein bereits laufendes Programm mit der angegebenen Prozess-ID.
- `-o <Datei>`: Leitet die Ausgabe in eine Datei um, anstatt sie auf der Konsole anzuzeigen.
- `-c`: Gibt eine Zusammenfassung der Systemaufrufe aus, anstatt sie einzeln aufzulisten.

## Häufige Beispiele
1. **Verfolgen eines neuen Programms:**
   ```bash
   strace ls
   ```
   Dieser Befehl verfolgt die Systemaufrufe, die beim Ausführen des `ls`-Befehls gemacht werden.

2. **Verfolgen eines laufenden Prozesses:**
   ```bash
   strace -p 1234
   ```
   Hierbei wird der Prozess mit der ID 1234 verfolgt.

3. **Ausgabe in eine Datei umleiten:**
   ```bash
   strace -o ausgabe.txt ls
   ```
   Dieser Befehl speichert die Ausgabe von `strace` in der Datei `ausgabe.txt`.

4. **Zusammenfassung der Systemaufrufe:**
   ```bash
   strace -c ls
   ```
   Mit dieser Option wird eine Zusammenfassung der Systemaufrufe für den `ls`-Befehl angezeigt.

## Tipps
- Verwenden Sie `strace` in Kombination mit `grep`, um spezifische Systemaufrufe zu filtern. Beispiel:
  ```bash
  strace ls 2>&1 | grep open
  ```
- Achten Sie darauf, dass das Verfolgen von Prozessen mit `strace` die Leistung beeinträchtigen kann, insbesondere bei stark frequentierten Anwendungen.
- Nutzen Sie die `-e` Option, um gezielt nur bestimmte Systemaufrufe zu verfolgen, was die Ausgabe übersichtlicher macht.