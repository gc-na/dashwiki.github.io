# [Deutsch] Debian Almquist Shell (dash) cmp Verwendung: Vergleiche zwei Dateien byteweise

## Übersicht
Der Befehl `cmp` wird verwendet, um zwei Dateien byteweise zu vergleichen. Er zeigt die erste Stelle an, an der sich die Dateien unterscheiden, und kann nützlich sein, um festzustellen, ob zwei Dateien identisch sind oder nicht.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
cmp [Optionen] [Datei1] [Datei2]
```

## Häufige Optionen
- `-l`: Gibt die Unterschiede zwischen den Dateien in Form von byteweisen Positionen aus.
- `-s`: Stummmodus; gibt keine Ausgabe aus, sondern nur den Exit-Status zurück.
- `-i N`: Ignoriert die ersten N Bytes der Dateien.
- `--help`: Zeigt eine Hilfeseite mit Informationen zur Verwendung von cmp an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `cmp`:

1. **Vergleiche zwei Dateien**:
   ```bash
   cmp datei1.txt datei2.txt
   ```

2. **Vergleiche zwei Dateien im Stummmodus**:
   ```bash
   cmp -s datei1.txt datei2.txt
   ```

3. **Gibt die Unterschiede in byteweisen Positionen aus**:
   ```bash
   cmp -l datei1.txt datei2.txt
   ```

4. **Ignoriere die ersten 10 Bytes der Dateien**:
   ```bash
   cmp -i 10 datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie den Stummmodus (`-s`), wenn Sie nur den Exit-Status benötigen, um zu überprüfen, ob die Dateien identisch sind.
- Nutzen Sie die Option `-l`, um detaillierte Informationen über die Unterschiede zwischen den Dateien zu erhalten.
- `cmp` ist besonders nützlich bei der Fehlersuche in Konfigurationsdateien oder bei der Überprüfung von Backups.