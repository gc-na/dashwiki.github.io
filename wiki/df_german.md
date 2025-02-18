# [Deutsch] Debian Almquist Shell (dash) df Verwendung: Zeigt den verfügbaren Speicherplatz auf Dateisystemen an

## Übersicht
Der Befehl `df` (disk free) wird verwendet, um Informationen über den verfügbaren und verwendeten Speicherplatz auf Dateisystemen anzuzeigen. Er gibt eine Übersicht über die Speicherkapazität von Dateisystemen, was besonders nützlich ist, um den verfügbaren Speicherplatz auf einem System zu überwachen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
df [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Zeigt die Größen in einem menschenlesbaren Format (z.B. KB, MB, GB) an.
- `-T`: Zeigt den Typ des Dateisystems an.
- `-a`: Zeigt alle Dateisysteme an, einschließlich der mit 0 Bytes belegten.
- `-i`: Zeigt Informationen über die Inodes an, anstatt über den Speicherplatz.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `df`-Befehls:

1. **Standardnutzung**: Zeigt die Speichernutzung für alle Dateisysteme an.
   ```bash
   df
   ```

2. **Menschenlesbares Format**: Zeigt die Speichernutzung in einem leicht verständlichen Format an.
   ```bash
   df -h
   ```

3. **Dateisystemtyp anzeigen**: Zeigt die Speichernutzung zusammen mit dem Typ des Dateisystems an.
   ```bash
   df -T
   ```

4. **Alle Dateisysteme anzeigen**: Zeigt auch die Dateisysteme mit 0 Bytes belegtem Speicher an.
   ```bash
   df -a
   ```

5. **Inode-Nutzung anzeigen**: Zeigt die Inode-Nutzung für alle Dateisysteme an.
   ```bash
   df -i
   ```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, insbesondere wenn Sie mit großen Speichermengen arbeiten.
- Überprüfen Sie regelmäßig den Speicherplatz, um sicherzustellen, dass Ihr System nicht überlastet wird.
- Kombinieren Sie `df` mit anderen Befehlen wie `grep`, um spezifische Informationen zu filtern, z.B. nur für das Root-Dateisystem:
  ```bash
  df -h | grep /
  ```