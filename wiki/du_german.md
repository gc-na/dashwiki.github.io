# [Deutsch] Debian Almquist Shell (dash) du: Speicherplatznutzung anzeigen

## Overview
Der Befehl `du` (Disk Usage) wird verwendet, um den Speicherplatzverbrauch von Dateien und Verzeichnissen im Dateisystem anzuzeigen. Er hilft Benutzern, herauszufinden, wie viel Speicherplatz von bestimmten Dateien oder Verzeichnissen belegt wird.

## Usage
Die grundlegende Syntax des Befehls `du` lautet:

```bash
du [Optionen] [Argumente]
```

## Common Options
Hier sind einige häufig verwendete Optionen für `du`:

- `-h`: Gibt die Größe in einem menschenlesbaren Format aus (z.B. KB, MB).
- `-s`: Zeigt nur die Gesamtsumme für jedes angegebene Argument an.
- `-a`: Listet auch die Größen von Dateien auf, nicht nur von Verzeichnissen.
- `-c`: Gibt eine Gesamtsumme für alle angegebenen Argumente aus.

## Common Examples
Hier sind einige praktische Beispiele zur Verwendung des Befehls `du`:

1. **Speicherplatznutzung eines Verzeichnisses anzeigen:**
   ```bash
   du /pfad/zum/verzeichnis
   ```

2. **Größen in menschenlesbarem Format anzeigen:**
   ```bash
   du -h /pfad/zum/verzeichnis
   ```

3. **Nur die Gesamtsumme eines Verzeichnisses anzeigen:**
   ```bash
   du -sh /pfad/zum/verzeichnis
   ```

4. **Alle Dateien und Verzeichnisse im aktuellen Verzeichnis auflisten:**
   ```bash
   du -a
   ```

5. **Gesamtsumme für mehrere Verzeichnisse anzeigen:**
   ```bash
   du -ch /pfad/zum/verzeichnis1 /pfad/zum/verzeichnis2
   ```

## Tips
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, insbesondere bei großen Datenmengen.
- Kombinieren Sie `du` mit `sort`, um die größten Verzeichnisse oder Dateien zuerst anzuzeigen:
  ```bash
  du -h /pfad/zum/verzeichnis | sort -hr
  ```
- Nutzen Sie `du` regelmäßig, um den Speicherplatzverbrauch zu überwachen und unnötige Dateien zu identifizieren.