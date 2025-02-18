# [Svenska] Debian Almquist Shell (dash) test användning: Kontrollera villkor

## Översikt
Kommandot `test` används för att utvärdera villkor och returnera ett statusvärde baserat på resultatet. Det är ofta använt i skript för att kontrollera om filer existerar, om variabler är tomma, eller för att jämföra värden.

## Användning
Den grundläggande syntaxen för kommandot är:

```sh
test [alternativ] [argument]
```

## Vanliga alternativ
- `-e`: Kontrollerar om en fil existerar.
- `-f`: Kontrollerar om en fil är en vanlig fil.
- `-d`: Kontrollerar om en fil är en katalog.
- `-z`: Kontrollerar om en sträng är tom.
- `=`: Jämför två strängar för likhet.
- `-lt`: Jämför två heltal för att se om det första är mindre än det andra.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `test`:

### Kontrollera om en fil existerar
```sh
if test -e fil.txt; then
    echo "Fil existerar."
else
    echo "Fil finns inte."
fi
```

### Kontrollera om en variabel är tom
```sh
variabel=""
if test -z "$variabel"; then
    echo "Variabeln är tom."
fi
```

### Jämföra två heltal
```sh
tal1=5
tal2=10
if test "$tal1" -lt "$tal2"; then
    echo "$tal1 är mindre än $tal2."
fi
```

### Kontrollera om en katalog existerar
```sh
if test -d /path/to/directory; then
    echo "Katalogen existerar."
else
    echo "Katalogen finns inte."
fi
```

## Tips
- Använd alltid citattecken runt variabler för att undvika problem med tomma värden.
- Du kan använda `[` som en synonym för `test`, vilket kan göra skript mer läsbara.
- Kombinera flera villkor med `-a` (och) eller `-o` (eller) för mer komplexa kontroller.