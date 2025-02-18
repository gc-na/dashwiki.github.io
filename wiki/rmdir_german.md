# [Deutsch] Debian Almquist Shell (dash) rmdir Verwendung: Verzeichnis entfernen

## Übersicht
Der Befehl `rmdir` wird verwendet, um leere Verzeichnisse im Dateisystem zu entfernen. Er löscht nur Verzeichnisse, die keine Dateien oder Unterverzeichnisse enthalten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
rmdir [Optionen] [Argumente]
```

## Häufige Optionen
- `--ignore-fail-on-non-empty`: Ignoriere Fehler, wenn das Verzeichnis nicht leer ist.
- `--verbose`: Zeige eine detaillierte Ausgabe über die durchgeführten Aktionen an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `rmdir`:

1. **Ein einzelnes leeres Verzeichnis entfernen**:
   ```bash
   rmdir mein_verzeichnis
   ```

2. **Mehrere leere Verzeichnisse auf einmal entfernen**:
   ```bash
   rmdir verzeichnis1 verzeichnis2 verzeichnis3
   ```

3. **Detaillierte Ausgabe beim Entfernen eines Verzeichnisses anzeigen**:
   ```bash
   rmdir --verbose mein_verzeichnis
   ```

4. **Fehler ignorieren, wenn das Verzeichnis nicht leer ist**:
   ```bash
   rmdir --ignore-fail-on-non-empty mein_verzeichnis
   ```

## Tipps
- Stellen Sie sicher, dass das Verzeichnis, das Sie entfernen möchten, wirklich leer ist, da `rmdir` nur leere Verzeichnisse löscht.
- Verwenden Sie `--verbose`, um zu bestätigen, dass das Verzeichnis erfolgreich entfernt wurde.
- Wenn Sie ein Verzeichnis mit Inhalten entfernen möchten, verwenden Sie den Befehl `rm -r` anstelle von `rmdir`.