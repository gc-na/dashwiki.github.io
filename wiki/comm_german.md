# [Deutsch] Debian Almquist Shell (dash) comm: Vergleiche zwei sortierte Dateien zeilenweise

## Übersicht
Der `comm` Befehl wird verwendet, um zwei sortierte Dateien zeilenweise zu vergleichen. Er zeigt die Unterschiede und Übereinstimmungen zwischen den beiden Dateien an, was besonders nützlich ist, um Änderungen oder Unterschiede in Textdateien zu identifizieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
comm [Optionen] [Datei1] [Datei2]
```

## Häufige Optionen
- `-1`: Unterdrückt die Ausgabe der Zeilen, die nur in der ersten Datei vorhanden sind.
- `-2`: Unterdrückt die Ausgabe der Zeilen, die nur in der zweiten Datei vorhanden sind.
- `-3`: Unterdrückt die Ausgabe der Zeilen, die in beiden Dateien vorhanden sind.
- `-i`: Ignoriert Groß- und Kleinschreibung beim Vergleich.
- `-d`: Gibt nur die Zeilen aus, die in beiden Dateien vorhanden sind.

## Häufige Beispiele

1. **Vergleich von zwei Dateien:**
   Um die Unterschiede zwischen zwei sortierten Dateien `file1.txt` und `file2.txt` anzuzeigen:
   ```bash
   comm file1.txt file2.txt
   ```

2. **Nur die Zeilen anzeigen, die in beiden Dateien vorhanden sind:**
   Um nur die gemeinsamen Zeilen anzuzeigen:
   ```bash
   comm -12 file1.txt file2.txt
   ```

3. **Zeilen aus der ersten Datei unterdrücken:**
   Um nur die Zeilen zu sehen, die in der zweiten Datei vorhanden sind:
   ```bash
   comm -13 file1.txt file2.txt
   ```

4. **Ignorieren der Groß- und Kleinschreibung:**
   Um den Vergleich ohne Berücksichtigung der Groß- und Kleinschreibung durchzuführen:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tipps
- Stellen Sie sicher, dass die Dateien vor der Verwendung von `comm` sortiert sind, da der Befehl nur mit sortierten Eingaben korrekt funktioniert.
- Nutzen Sie die Optionen `-1`, `-2` und `-3`, um die Ausgabe nach Ihren Bedürfnissen anzupassen und nur die relevanten Informationen anzuzeigen.
- Verwenden Sie `sort` in Kombination mit `comm`, um schnell Unterschiede zwischen unsortierten Dateien zu finden:
  ```bash
  comm <(sort file1.txt) <(sort file2.txt)
  ```