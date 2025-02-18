# [Deutsch] Debian Almquist Shell (dash) sed Verwendung: Textbearbeitung im Stream

## Übersicht
Der `sed`-Befehl (Stream Editor) ist ein leistungsstarkes Werkzeug zur Bearbeitung von Textströmen. Er ermöglicht das Suchen, Ersetzen, Einfügen und Löschen von Text in Dateien oder von Eingabeströmen, ohne die Originaldatei zu verändern.

## Verwendung
Die grundlegende Syntax des `sed`-Befehls lautet:

```bash
sed [Optionen] [Argumente]
```

## Häufige Optionen
- `-e`: Ermöglicht das Angeben mehrerer Bearbeitungsanweisungen.
- `-i`: Führt die Bearbeitung direkt in der Datei durch (in-place).
- `-n`: Unterdrückt die Standardausgabe, sodass nur die explizit angegebenen Ausgaben angezeigt werden.
- `s/pattern/replacement/`: Führt eine Ersetzung durch, wobei `pattern` das zu suchende Muster und `replacement` der Ersatztext ist.

## Häufige Beispiele

### 1. Einfaches Ersetzen
Um das Wort "alt" durch "neu" in einer Datei zu ersetzen, verwenden Sie:

```bash
sed 's/alt/neu/' datei.txt
```

### 2. Ersetzen in der Datei
Um das Wort "alt" durch "neu" direkt in der Datei zu ersetzen, verwenden Sie:

```bash
sed -i 's/alt/neu/' datei.txt
```

### 3. Mehrere Ersetzungen
Um mehrere Ersetzungen in einer Datei durchzuführen, können Sie die `-e` Option verwenden:

```bash
sed -e 's/alt/neu/' -e 's/rot/blau/' datei.txt
```

### 4. Zeilen löschen
Um alle Zeilen, die das Wort "löschen" enthalten, auszugeben, verwenden Sie:

```bash
sed '/löschen/d' datei.txt
```

### 5. Nur bestimmte Zeilen anzeigen
Um nur die Zeilen 2 bis 4 einer Datei anzuzeigen, verwenden Sie:

```bash
sed -n '2,4p' datei.txt
```

## Tipps
- Testen Sie Ihre `sed`-Befehle zuerst ohne die `-i`-Option, um sicherzustellen, dass die gewünschten Änderungen korrekt sind.
- Nutzen Sie reguläre Ausdrücke für komplexere Suchmuster.
- Kombinieren Sie `sed` mit anderen Befehlen wie `grep` oder `awk` für erweiterte Textverarbeitungen.