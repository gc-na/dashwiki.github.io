# [Deutsch] Debian Almquist Shell (dash) shift Verwendung: Argumente verschieben

## Übersicht
Der `shift` Befehl in der Debian Almquist Shell (dash) wird verwendet, um die Positionsparameter in einem Shell-Skript zu verschieben. Dies bedeutet, dass die Argumente, die an das Skript übergeben wurden, nach links verschoben werden, sodass die Anzahl der Argumente, die zur Verfügung stehen, verringert wird.

## Verwendung
Die grundlegende Syntax des `shift` Befehls sieht folgendermaßen aus:

```sh
shift [n]
```

Hierbei ist `n` die Anzahl der Positionen, um die die Argumente verschoben werden sollen. Wenn `n` nicht angegeben wird, wird standardmäßig um eins verschoben.

## Häufige Optionen
- `n`: Gibt die Anzahl der Positionen an, um die die Argumente verschoben werden sollen. Wenn `n` nicht angegeben wird, wird um eins verschoben.

## Häufige Beispiele

### Beispiel 1: Einfaches Verschieben
```sh
#!/bin/dash
set -- a b c d
echo "Vor shift: $1 $2 $3 $4"
shift
echo "Nach shift: $1 $2 $3 $4"
```
**Ausgabe:**
```
Vor shift: a b c d
Nach shift: b c d
```

### Beispiel 2: Mehrfaches Verschieben
```sh
#!/bin/dash
set -- 1 2 3 4 5
echo "Vor shift: $1 $2 $3 $4 $5"
shift 2
echo "Nach shift: $1 $2 $3 $4 $5"
```
**Ausgabe:**
```
Vor shift: 1 2 3 4 5
Nach shift: 3 4 5
```

### Beispiel 3: Verwendung in einem Skript
```sh
#!/bin/dash
for arg in "$@"; do
    echo "Aktuelles Argument: $arg"
    shift
done
```
Wenn das Skript mit den Argumenten `a b c` aufgerufen wird, wird die Ausgabe sein:
```
Aktuelles Argument: a
Aktuelles Argument: b
Aktuelles Argument: c
```

## Tipps
- Verwenden Sie `shift` in Schleifen, um alle übergebenen Argumente nacheinander zu verarbeiten.
- Achten Sie darauf, dass nach dem Verschieben von Argumenten die Anzahl der verbleibenden Argumente überprüft wird, um Fehler zu vermeiden.
- Nutzen Sie `set --` am Anfang eines Skripts, um die Argumente klar zu definieren, bevor Sie `shift` verwenden.