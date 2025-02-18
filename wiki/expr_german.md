# [Deutsch] Debian Almquist Shell (dash) expr Verwendung: Berechnungen und String-Manipulationen

## Overview
Der `expr` Befehl in der Debian Almquist Shell (dash) wird verwendet, um einfache Berechnungen durchzuführen und Zeichenfolgen zu manipulieren. Er kann mathematische Ausdrücke auswerten und grundlegende String-Operationen wie das Extrahieren von Substrings oder das Vergleichen von Zeichenfolgen durchführen.

## Usage
Die grundlegende Syntax des `expr` Befehls lautet:

```sh
expr [Optionen] [Argumente]
```

## Common Options
Hier sind einige gängige Optionen für `expr`:

- `+` : Addition von zwei Zahlen.
- `-` : Subtraktion von zwei Zahlen.
- `*` : Multiplikation von zwei Zahlen (muss mit Escape-Zeichen `\*` verwendet werden).
- `/` : Division von zwei Zahlen.
- `%` : Modulo-Operation (Rest einer Division).
- `=` : Vergleicht zwei Zeichenfolgen auf Gleichheit.
- `:` : Extrahiert einen Teil einer Zeichenfolge.

## Common Examples
Hier sind einige praktische Beispiele für die Verwendung von `expr`:

### Beispiel 1: Einfache Addition
```sh
expr 5 + 3
```
Ausgabe: `8`

### Beispiel 2: Subtraktion
```sh
expr 10 - 4
```
Ausgabe: `6`

### Beispiel 3: Multiplikation
```sh
expr 5 \* 2
```
Ausgabe: `10`

### Beispiel 4: Division
```sh
expr 20 / 4
```
Ausgabe: `5`

### Beispiel 5: Modulo
```sh
expr 10 % 3
```
Ausgabe: `1`

### Beispiel 6: String-Vergleich
```sh
expr "Hallo" = "Hallo"
```
Ausgabe: `1` (wahr)

### Beispiel 7: Substring-Extraktion
```sh
expr substr "Hallo Welt" 1 5
```
Ausgabe: `Hallo`

## Tips
- Achten Sie darauf, mathematische Operatoren wie `*` mit einem Escape-Zeichen `\` zu verwenden, um Missverständnisse mit Shell-Interpretationen zu vermeiden.
- Verwenden Sie Klammern, um die Reihenfolge der Operationen in komplexeren Ausdrücken zu steuern.
- `expr` gibt standardmäßig keine Fehlercodes zurück, wenn ein Fehler auftritt. Überprüfen Sie daher die Ausgabe sorgfältig.