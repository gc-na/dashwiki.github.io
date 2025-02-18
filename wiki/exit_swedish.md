# [Svenska] Debian Almquist Shell (dash) exit användning: Avsluta ett skript eller en session

## Översikt
Kommandot `exit` används för att avsluta ett skript eller en session i Debian Almquist Shell (dash). Det kan också returnera ett statusvärde till den omgivande miljön, vilket kan vara användbart för att indikera om skriptet kördes framgångsrikt eller om det uppstod ett fel.

## Användning
Den grundläggande syntaxen för kommandot är:

```sh
exit [status]
```

Där `status` är ett valfritt heltal som representerar avslutningsstatusen.

## Vanliga alternativ
- `status`: Ett heltal mellan 0 och 255 som anger avslutningsstatusen. Standardvärdet är 0, vilket indikerar att skriptet avslutades utan fel.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `exit`:

### Exempel 1: Avsluta ett skript utan fel
```sh
#!/bin/dash
echo "Skriptet körs."
exit 0
```

### Exempel 2: Avsluta ett skript med ett fel
```sh
#!/bin/dash
echo "Ett fel inträffade."
exit 1
```

### Exempel 3: Använda exit i en funktion
```sh
#!/bin/dash
my_function() {
    echo "Kör funktion."
    exit 2
}

my_function
```

## Tips
- Använd alltid `exit 0` för att indikera att skriptet avslutades framgångsrikt.
- Använd olika statuskoder för att representera olika feltyper, vilket kan hjälpa vid felsökning.
- Tänk på att om du kör `exit` i en terminalsession, kommer hela sessionen att stängas.