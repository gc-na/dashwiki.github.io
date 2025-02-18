# [Deutsch] Debian Almquist Shell (dash) xargs Verwendung: Befehle verarbeiten und an andere Programme übergeben

## Übersicht
Der `xargs` Befehl wird verwendet, um Eingaben von Standard- oder Dateiströmen zu lesen und sie als Argumente an andere Befehle zu übergeben. Dies ist besonders nützlich, wenn die Anzahl der Argumente zu groß ist, um sie direkt in einem Befehl zu verwenden.

## Verwendung
Die grundlegende Syntax des `xargs` Befehls lautet:

```bash
xargs [Optionen] [Befehle]
```

## Häufige Optionen
- `-n N`: Gibt an, dass maximal N Argumente pro Befehl verwendet werden sollen.
- `-d DELIMITER`: Legt ein benutzerdefiniertes Trennzeichen für die Eingabe fest.
- `-0`: Erwartet, dass die Eingaben nullterminiert sind (nützlich mit `find -print0`).
- `-p`: Fragt vor der Ausführung jedes Befehls um Bestätigung.
- `-I {}`: Ersetzt `{}` durch die Eingabe in dem angegebenen Befehl.

## Häufige Beispiele

### Beispiel 1: Dateien löschen
Um alle `.tmp` Dateien im aktuellen Verzeichnis zu löschen:

```bash
find . -name "*.tmp" | xargs rm
```

### Beispiel 2: Begrenzte Argumente
Um maximal 3 Dateien gleichzeitig zu kopieren:

```bash
find . -name "*.jpg" | xargs -n 3 cp -t /zielverzeichnis/
```

### Beispiel 3: Benutzerdefiniertes Trennzeichen
Wenn die Eingaben durch Kommas getrennt sind:

```bash
echo "datei1,datei2,datei3" | xargs -d ',' cp -t /zielverzeichnis/
```

### Beispiel 4: Nullterminierte Eingaben
Um mit nullterminierten Dateinamen umzugehen:

```bash
find . -name "*.txt" -print0 | xargs -0 wc -l
```

## Tipps
- Verwenden Sie `-n`, um die Anzahl der Argumente zu steuern und die Belastung des Systems zu minimieren.
- Nutzen Sie `-I {}`, um komplexe Befehle mit Platzhaltern zu erstellen.
- Testen Sie Ihre Befehle zuerst mit `echo`, um zu sehen, welche Argumente übergeben werden, bevor Sie sie tatsächlich ausführen.