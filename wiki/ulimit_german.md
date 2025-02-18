# [Deutsch] Debian Almquist Shell (dash) ulimit Verwendung: Begrenzung von Ressourcen

## Übersicht
Der Befehl `ulimit` wird verwendet, um die Ressourcenlimits für Benutzerprozesse in der Shell festzulegen oder abzurufen. Dies hilft, die Systemressourcen zu verwalten und zu verhindern, dass ein einzelner Prozess übermäßig viele Ressourcen verbraucht.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
ulimit [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle aktuellen Limits an.
- `-c`: Setzt die maximale Größe von Kerneldumps.
- `-d`: Setzt die maximale Größe des Datensegments.
- `-f`: Setzt die maximale Größe von Dateien, die erstellt werden können.
- `-l`: Setzt die maximale Größe von gelocktem Speicher.
- `-m`: Setzt die maximale Größe des physischen Speichers.
- `-n`: Setzt die maximale Anzahl von offenen Dateien.
- `-s`: Setzt die maximale Größe des Stapels.
- `-t`: Setzt die maximale CPU-Zeit in Sekunden.
- `-v`: Setzt die maximale Größe des virtuellen Speichers.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `ulimit`:

1. **Alle aktuellen Limits anzeigen:**
   ```bash
   ulimit -a
   ```

2. **Maximale Anzahl von offenen Dateien erhöhen:**
   ```bash
   ulimit -n 1024
   ```

3. **Maximale Größe von Dateien auf 10 MB setzen:**
   ```bash
   ulimit -f 10240
   ```

4. **Maximale CPU-Zeit auf 30 Sekunden setzen:**
   ```bash
   ulimit -t 30
   ```

5. **Maximale Größe des Stapels auf 8 MB setzen:**
   ```bash
   ulimit -s 8192
   ```

## Tipps
- Überprüfen Sie die aktuellen Limits mit `ulimit -a`, bevor Sie Änderungen vornehmen.
- Stellen Sie sicher, dass Sie die Limits nicht so niedrig setzen, dass wichtige Prozesse beeinträchtigt werden.
- Änderungen, die mit `ulimit` vorgenommen werden, gelten nur für die aktuelle Shell-Sitzung. Um sie dauerhaft zu machen, fügen Sie die Befehle in Ihre Shell-Konfigurationsdatei (z. B. `.bashrc` oder `.profile`) ein.