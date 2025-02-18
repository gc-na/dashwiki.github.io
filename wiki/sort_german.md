# [Deutsch] Debian Almquist Shell (dash) sort Verwendung: Sortieren von Zeilen in Textdateien

## Übersicht
Der Befehl `sort` wird verwendet, um die Zeilen einer Textdatei oder einer Eingabe nach bestimmten Kriterien zu sortieren. Er kann alphabetisch, numerisch oder nach benutzerdefinierten Regeln sortieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
sort [Optionen] [Argumente]
```

## Häufige Optionen
- `-n`: Sortiert numerisch.
- `-r`: Sortiert in umgekehrter Reihenfolge.
- `-k`: Gibt das Sortierfeld an (z.B. `-k 2` sortiert nach der zweiten Spalte).
- `-u`: Entfernt doppelte Zeilen.
- `-o`: Gibt die Ausgabedatei an (z.B. `-o ausgabe.txt`).

## Häufige Beispiele
- **Einfaches Sortieren einer Datei:**
  ```bash
  sort datei.txt
  ```

- **Sortieren mit umgekehrter Reihenfolge:**
  ```bash
  sort -r datei.txt
  ```

- **Numerisches Sortieren:**
  ```bash
  sort -n zahlen.txt
  ```

- **Sortieren nach einer bestimmten Spalte:**
  ```bash
  sort -k 2 daten.txt
  ```

- **Sortieren und Ausgaben in eine neue Datei schreiben:**
  ```bash
  sort -o sortierte_datei.txt datei.txt
  ```

## Tipps
- Verwenden Sie die Option `-u`, um doppelte Zeilen zu entfernen und nur eindeutige Zeilen zu behalten.
- Kombinieren Sie `sort` mit anderen Befehlen wie `uniq`, um die Ausgabe weiter zu verarbeiten.
- Experimentieren Sie mit verschiedenen Optionen, um die Sortierung an Ihre Bedürfnisse anzupassen.