# [Deutsch] Debian Almquist Shell (dash) tee Verwendung: Daten in Dateien und auf der Konsole ausgeben

## Übersicht
Der `tee`-Befehl in der Debian Almquist Shell (dash) wird verwendet, um Eingabedaten sowohl in eine oder mehrere Dateien zu schreiben als auch gleichzeitig auf der Standardausgabe (normalerweise dem Terminal) anzuzeigen. Dies ist besonders nützlich, wenn Sie den Output eines Befehls überwachen und gleichzeitig in einer Datei speichern möchten.

## Verwendung
Die grundlegende Syntax des `tee`-Befehls lautet:

```bash
tee [Optionen] [Datei(en)]
```

## Häufige Optionen
- `-a` oder `--append`: Fügt die Ausgabe an die angegebene Datei an, anstatt sie zu überschreiben.
- `-i` oder `--ignore-interrupts`: Ignoriert Interrupt-Signale.
- `--help`: Zeigt eine Hilfemeldung mit den verfügbaren Optionen an.
- `--version`: Gibt die Versionsnummer des `tee`-Befehls aus.

## Häufige Beispiele

### Beispiel 1: Einfaches Schreiben in eine Datei
Um die Ausgabe eines Befehls in eine Datei zu schreiben und gleichzeitig anzuzeigen, können Sie Folgendes verwenden:

```bash
echo "Hallo Welt" | tee ausgabe.txt
```

### Beispiel 2: Anhängen an eine bestehende Datei
Um Daten an eine bereits bestehende Datei anzuhängen, verwenden Sie die `-a`-Option:

```bash
echo "Zusätzliche Zeile" | tee -a ausgabe.txt
```

### Beispiel 3: Ausgabe mehrerer Dateien
Sie können die Ausgabe auch in mehrere Dateien gleichzeitig schreiben:

```bash
echo "Daten für mehrere Dateien" | tee datei1.txt datei2.txt
```

### Beispiel 4: Kombination mit anderen Befehlen
`tee` kann auch in Kombination mit anderen Befehlen verwendet werden. Zum Beispiel, um die Ausgabe von `ls` in eine Datei zu schreiben und gleichzeitig anzuzeigen:

```bash
ls -l | tee verzeichnis_inhalt.txt
```

## Tipps
- Verwenden Sie die `-a`-Option, wenn Sie sicherstellen möchten, dass bestehende Daten in einer Datei nicht überschrieben werden.
- Kombinieren Sie `tee` mit anderen Befehlen in einer Pipeline, um die Ausgabe flexibel zu verarbeiten.
- Nutzen Sie `tee` in Skripten, um Debugging-Informationen zu speichern, während das Skript ausgeführt wird.