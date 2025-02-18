# [Deutsch] Debian Almquist Shell (dash) basename Verwendung: Entfernen von Pfad und Suffix

## Overview
Der Befehl `basename` wird verwendet, um den Dateinamen aus einem vollständigen Pfad zu extrahieren. Er entfernt den Verzeichnispfad und kann auch eine angegebene Dateiendung (Suffix) entfernen.

## Usage
Die grundlegende Syntax des Befehls lautet:

```bash
basename [Optionen] [Argumente]
```

## Common Options
- `-a`: Verarbeitet mehrere Argumente und gibt die Basen für jedes Argument zurück.
- `-s Suffix`: Entfernt das angegebene Suffix vom Dateinamen.

## Common Examples

### Beispiel 1: Basisnamen aus einem Pfad extrahieren
Um den Basisnamen einer Datei zu erhalten, verwenden Sie:

```bash
basename /usr/local/bin/script.sh
```
Ausgabe:
```
script.sh
```

### Beispiel 2: Basisnamen ohne Suffix
Um den Basisnamen ohne die Dateiendung zu erhalten, verwenden Sie:

```bash
basename /usr/local/bin/script.sh .sh
```
Ausgabe:
```
script
```

### Beispiel 3: Mehrere Argumente verarbeiten
Um die Basisnamen mehrerer Dateien zu extrahieren, verwenden Sie die `-a` Option:

```bash
basename -a /usr/local/bin/script.sh /usr/bin/another_script.py
```
Ausgabe:
```
script.sh
another_script.py
```

### Beispiel 4: Suffix von mehreren Dateien entfernen
Um das Suffix von mehreren Dateien zu entfernen, können Sie Folgendes tun:

```bash
basename -s .txt /home/user/file1.txt /home/user/file2.txt
```
Ausgabe:
```
file1
file2
```

## Tips
- Verwenden Sie `basename` in Skripten, um Dateinamen dynamisch zu verarbeiten.
- Kombinieren Sie `basename` mit anderen Befehlen wie `find`, um gezielt Dateinamen zu extrahieren.
- Achten Sie darauf, das Suffix korrekt anzugeben, um unerwartete Ergebnisse zu vermeiden.