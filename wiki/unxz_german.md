# [Deutsch] Debian Almquist Shell (dash) unxz Verwendung: Entpacken von .xz-Dateien

## Übersicht
Der Befehl `unxz` wird verwendet, um Dateien im .xz-Format zu entpacken. Dies ist ein gängiges Komprimierungsformat, das häufig für die Verteilung von Software und Daten verwendet wird.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
unxz [Optionen] [Argumente]
```

## Häufige Optionen
- `-k`, `--keep`: Behalte die komprimierte Datei nach dem Entpacken.
- `-f`, `--force`: Überschreibe vorhandene Dateien ohne Nachfrage.
- `-v`, `--verbose`: Zeige detaillierte Informationen während des Entpackens an.

## Häufige Beispiele
Um eine Datei namens `beispiel.xz` zu entpacken, verwenden Sie einfach:

```bash
unxz beispiel.xz
```

Wenn Sie die komprimierte Datei behalten möchten, können Sie den `-k` Schalter verwenden:

```bash
unxz -k beispiel.xz
```

Um eine Datei mit dem `-f` Schalter zu entpacken, der vorhandene Dateien überschreibt, verwenden Sie:

```bash
unxz -f beispiel.xz
```

Für detaillierte Ausgaben während des Entpackens können Sie den `-v` Schalter hinzufügen:

```bash
unxz -v beispiel.xz
```

## Tipps
- Überprüfen Sie immer den Speicherplatz auf Ihrer Festplatte, bevor Sie große .xz-Dateien entpacken, um sicherzustellen, dass genügend Platz vorhanden ist.
- Nutzen Sie den `-k` Schalter, wenn Sie die Originaldatei für zukünftige Referenzen behalten möchten.
- Wenn Sie regelmäßig mit .xz-Dateien arbeiten, können Sie Aliase in Ihrer Shell-Konfiguration einrichten, um häufig verwendete Optionen zu vereinfachen.