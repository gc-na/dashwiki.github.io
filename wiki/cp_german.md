# [Deutsch] Debian Almquist Shell (dash) cp Verwendung: Dateien kopieren

## Übersicht
Der `cp`-Befehl wird verwendet, um Dateien und Verzeichnisse in der Debian Almquist Shell (dash) zu kopieren. Er ermöglicht es Benutzern, eine oder mehrere Quelldateien an einen Zielort zu kopieren.

## Verwendung
Die grundlegende Syntax des `cp`-Befehls lautet:

```bash
cp [Optionen] [Argumente]
```

## Häufige Optionen
- `-r`: Kopiert Verzeichnisse rekursiv.
- `-i`: Fragt vor dem Überschreiben einer bestehenden Datei nach.
- `-u`: Kopiert nur, wenn die Quelldatei neuer ist als die Zieldatei oder wenn die Zieldatei nicht existiert.
- `-v`: Gibt detaillierte Informationen über den Kopiervorgang aus.

## Häufige Beispiele
1. **Einzelne Datei kopieren:**
   ```bash
   cp datei.txt kopie_datei.txt
   ```

2. **Mehrere Dateien in ein Verzeichnis kopieren:**
   ```bash
   cp datei1.txt datei2.txt /zielverzeichnis/
   ```

3. **Verzeichnis rekursiv kopieren:**
   ```bash
   cp -r /quellverzeichnis/ /zielverzeichnis/
   ```

4. **Kopieren mit Bestätigung vor dem Überschreiben:**
   ```bash
   cp -i datei.txt kopie_datei.txt
   ```

5. **Nur neuere Dateien kopieren:**
   ```bash
   cp -u datei.txt /zielverzeichnis/
   ```

## Tipps
- Verwenden Sie die `-i`-Option, um versehentliches Überschreiben wichtiger Dateien zu vermeiden.
- Nutzen Sie die `-v`-Option, um den Fortschritt des Kopiervorgangs zu verfolgen, besonders bei großen Dateien oder Verzeichnissen.
- Überprüfen Sie vor dem Kopieren den Zielort, um sicherzustellen, dass Sie die Dateien an den richtigen Ort verschieben.