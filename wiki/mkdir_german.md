# [Deutsch] Debian Almquist Shell (dash) mkdir Verwendung: Verzeichnisse erstellen

## Übersicht
Der Befehl `mkdir` wird verwendet, um neue Verzeichnisse im Dateisystem zu erstellen. Er ist ein grundlegendes Werkzeug in der Shell, das es Benutzern ermöglicht, die Struktur ihrer Dateien und Ordner zu organisieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
mkdir [Optionen] [Argumente]
```

## Häufige Optionen
- `-p`: Erstellt das Verzeichnis und alle übergeordneten Verzeichnisse, die nicht existieren.
- `-m`: Setzt die Berechtigungen für das neu erstellte Verzeichnis.
- `-v`: Gibt eine ausführliche Ausgabe aus, die anzeigt, welche Verzeichnisse erstellt wurden.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `mkdir`:

1. Ein einfaches Verzeichnis erstellen:
   ```bash
   mkdir mein_verzeichnis
   ```

2. Mehrere Verzeichnisse gleichzeitig erstellen:
   ```bash
   mkdir verzeichnis1 verzeichnis2 verzeichnis3
   ```

3. Ein Verzeichnis mit übergeordneten Verzeichnissen erstellen:
   ```bash
   mkdir -p /home/benutzer/neues_verzeichnis/unterverzeichnis
   ```

4. Ein Verzeichnis mit bestimmten Berechtigungen erstellen:
   ```bash
   mkdir -m 755 mein_sicheres_verzeichnis
   ```

5. Eine ausführliche Ausgabe beim Erstellen eines Verzeichnisses anzeigen:
   ```bash
   mkdir -v mein_verzeichnis
   ```

## Tipps
- Verwenden Sie die `-p` Option, um sicherzustellen, dass alle übergeordneten Verzeichnisse erstellt werden, ohne Fehler zu verursachen, wenn sie bereits existieren.
- Überprüfen Sie die Berechtigungen des Verzeichnisses mit `ls -l`, um sicherzustellen, dass sie Ihren Anforderungen entsprechen.
- Nutzen Sie die ausführliche Ausgabe (`-v`), um zu bestätigen, dass Ihre Verzeichnisse erfolgreich erstellt wurden, insbesondere wenn Sie mehrere Verzeichnisse auf einmal erstellen.