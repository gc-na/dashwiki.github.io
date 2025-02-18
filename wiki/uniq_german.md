# [Deutsch] Debian Almquist Shell (dash) uniq Verwendung: Entfernen von aufeinanderfolgenden Duplikaten in einer Datei

## Übersicht
Der Befehl `uniq` wird verwendet, um aufeinanderfolgende doppelte Zeilen aus einer Datei oder von der Standardeingabe zu entfernen. Dies ist besonders nützlich, um Daten zu bereinigen und nur eindeutige Einträge anzuzeigen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
uniq [Optionen] [Argumente]
```

## Häufige Optionen
- `-c`: Zählt die Anzahl der Vorkommen jeder Zeile und gibt diese zusammen mit der Zeile aus.
- `-d`: Gibt nur die Zeilen aus, die mehr als einmal vorkommen.
- `-u`: Gibt nur die Zeilen aus, die einzigartig sind (d.h. nur einmal vorkommen).
- `-i`: Ignoriert Groß- und Kleinschreibung bei der Duplikatsprüfung.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `uniq`:

1. **Entfernen von Duplikaten aus einer Datei:**
   ```bash
   uniq datei.txt
   ```

2. **Zählen der Vorkommen jeder Zeile:**
   ```bash
   uniq -c datei.txt
   ```

3. **Anzeigen nur der doppelten Zeilen:**
   ```bash
   uniq -d datei.txt
   ```

4. **Anzeigen nur der einzigartigen Zeilen:**
   ```bash
   uniq -u datei.txt
   ```

5. **Ignorieren der Groß- und Kleinschreibung:**
   ```bash
   uniq -i datei.txt
   ```

## Tipps
- Stellen Sie sicher, dass die Eingabedaten sortiert sind, da `uniq` nur aufeinanderfolgende Duplikate entfernt. Verwenden Sie den Befehl `sort`, um die Daten vorher zu sortieren.
- Kombinieren Sie `uniq` mit anderen Befehlen in einer Pipeline, um komplexe Datenverarbeitungen durchzuführen. Zum Beispiel:
  ```bash
  sort datei.txt | uniq
  ```
- Nutzen Sie die Option `-c`, um schnell einen Überblick über die Häufigkeit von Einträgen zu erhalten, was bei der Analyse von Daten hilfreich sein kann.