# [Norsk] Debian Almquist Shell (dash) shift bruken: Flytt posisjonsparametere

## Oversikt
`shift`-kommandoen i dash brukes til å flytte posisjonsparametere til venstre. Dette betyr at den første parameteren (posisjon 1) fjernes, og de gjenværende parameterne flyttes opp ett nivå. Dette er nyttig når du ønsker å håndtere argumenter i skriptene dine på en mer dynamisk måte.

## Bruk
Grunnleggende syntaks for `shift`-kommandoen er som følger:

```sh
shift [n]
```

Her er `n` antall posisjonsparametere som skal flyttes. Hvis `n` ikke spesifiseres, flyttes én parameter som standard.

## Vanlige alternativer
- `n`: Angir hvor mange posisjonsparametere som skal flyttes. Hvis `n` er større enn antall tilgjengelige parametere, vil alle bli flyttet.

## Vanlige eksempler

### Eksempel 1: Flytte én parameter
```sh
#!/bin/dash
set -- a b c d
echo "Før shift: $1 $2 $3 $4"
shift
echo "Etter shift: $1 $2 $3 $4"
```
Utdata:
```
Før shift: a b c d
Etter shift: b c d
```

### Eksempel 2: Flytte flere parametere
```sh
#!/bin/dash
set -- 1 2 3 4 5
echo "Før shift: $1 $2 $3 $4 $5"
shift 2
echo "Etter shift: $1 $2 $3 $4 $5"
```
Utdata:
```
Før shift: 1 2 3 4 5
Etter shift: 3 4 5
```

### Eksempel 3: Håndtere ukjente antall parametere
```sh
#!/bin/dash
set -- "$@"
while [ "$#" -gt 0 ]; do
    echo "Behandler: $1"
    shift
done
```
Her vil skriptet behandle alle argumentene som ble sendt til det, ett om gangen.

## Tips
- Bruk `shift` i løkker for å håndtere variable antall argumenter effektivt.
- Vær oppmerksom på at `shift` endrer posisjonsparametrene, så vær sikker på at du har lagret verdiene du trenger før du bruker det.
- Kombiner `shift` med andre kommandoer som `case` for mer kompleks argumentbehandling i skriptene dine.