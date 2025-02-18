# [Deutsch] Debian Almquist Shell (dash) diff Verwendung: Unterschiede zwischen Dateien anzeigen

## Übersicht
Der `diff`-Befehl wird verwendet, um die Unterschiede zwischen zwei Dateien oder Verzeichnissen anzuzeigen. Er vergleicht den Inhalt der Dateien und gibt die Zeilen aus, die sich unterscheiden, was besonders nützlich ist, um Änderungen in Textdateien zu verfolgen.

## Verwendung
Die grundlegende Syntax des `diff`-Befehls lautet:

```bash
diff [Optionen] [Argumente]
```

## Häufige Optionen
- `-u`: Zeigt die Unterschiede im Unified-Format an, das leichter zu lesen ist.
- `-c`: Gibt die Unterschiede im kontextuellen Format aus.
- `-i`: Ignoriert Groß- und Kleinschreibung bei der Vergleichung.
- `-w`: Ignoriert Leerzeichen und Tabulatoren.
- `-r`: Vergleicht Verzeichnisse rekursiv.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `diff`-Befehls:

1. **Einfacher Vergleich zweier Dateien**:
   ```bash
   diff datei1.txt datei2.txt
   ```

2. **Vergleich im Unified-Format**:
   ```bash
   diff -u datei1.txt datei2.txt
   ```

3. **Vergleich zweier Verzeichnisse rekursiv**:
   ```bash
   diff -r verzeichnis1/ verzeichnis2/
   ```

4. **Ignorieren von Leerzeichen**:
   ```bash
   diff -w datei1.txt datei2.txt
   ```

## Tipps
- Verwenden Sie die Option `-u`, um die Ausgabe leserlicher zu gestalten, insbesondere wenn Sie Änderungen in Code-Dateien überprüfen.
- Nutzen Sie `diff` zusammen mit `patch`, um Änderungen an Dateien anzuwenden, die Sie mit `diff` erstellt haben.
- Speichern Sie die Ausgabe von `diff` in einer Datei, um die Unterschiede später zu überprüfen:
  ```bash
  diff datei1.txt datei2.txt > unterschiede.txt
  ```