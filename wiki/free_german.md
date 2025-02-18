# [Deutsch] Debian Almquist Shell (dash) free Befehl: Zeigt Speicherinformationen an

## Übersicht
Der `free`-Befehl zeigt Informationen über den verfügbaren und verwendeten Speicher in einem Linux-System an. Er ist nützlich, um einen schnellen Überblick über den Arbeitsspeicher (RAM) und den Swap-Speicher zu erhalten.

## Verwendung
Die grundlegende Syntax des `free`-Befehls lautet:

```bash
free [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Gibt die Speicherwerte in einem menschenlesbaren Format aus (z.B. in MB oder GB).
- `-m`: Zeigt die Speichermengen in Megabyte an.
- `-g`: Zeigt die Speichermengen in Gigabyte an.
- `-s <Sekunden>`: Aktualisiert die Ausgabe alle angegebenen Sekunden.
- `-t`: Zeigt eine Zeile mit der Gesamtsumme des Speichers an.

## Häufige Beispiele
Um die grundlegenden Speicherinformationen anzuzeigen, verwenden Sie einfach:

```bash
free
```

Um die Informationen in einem menschenlesbaren Format anzuzeigen:

```bash
free -h
```

Um die Speichermengen in Megabyte anzuzeigen:

```bash
free -m
```

Um die Ausgabe alle 5 Sekunden zu aktualisieren:

```bash
free -s 5
```

Um die Gesamtsumme des Speichers anzuzeigen:

```bash
free -t
```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, besonders wenn Sie mit großen Speichermengen arbeiten.
- Kombinieren Sie `free` mit anderen Befehlen wie `watch`, um die Speicherverwendung in Echtzeit zu überwachen: 

```bash
watch free -h
```

- Nutzen Sie `free` regelmäßig, um den Zustand Ihres Systems zu überwachen und Engpässe im Speicher frühzeitig zu erkennen.