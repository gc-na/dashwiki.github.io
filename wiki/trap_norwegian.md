# [Norsk] Debian Almquist Shell (dash) trap bruk: Håndter signaler og avslutninger

## Oversikt
`trap`-kommandoen i dash brukes til å håndtere signaler og avslutninger i skript. Den lar deg spesifisere kommandoer som skal kjøres når et bestemt signal mottas, noe som kan være nyttig for å rydde opp ressurser eller utføre spesifikke oppgaver før skriptet avsluttes.

## Bruk
Den grunnleggende syntaksen for `trap`-kommandoen er som følger:

```sh
trap [kommando] [signal]
```

## Vanlige alternativer
- `SIGINT`: Signal for avbrudd (Ctrl+C).
- `SIGTERM`: Signal for å be om avslutning.
- `EXIT`: Kjør kommandoen når skriptet avsluttes.

## Vanlige eksempler

### Eksempel 1: Håndtere SIGINT
Dette eksemplet viser hvordan du kan håndtere avbruddssignalet (Ctrl+C):

```sh
trap 'echo "Skriptet ble avbrutt"; exit' SIGINT
while true; do
    echo "Kjører skript... Trykk Ctrl+C for å avbryte."
    sleep 1
done
```

### Eksempel 2: Rydde opp ved avslutning
Her er et eksempel på hvordan du kan rydde opp når skriptet avsluttes:

```sh
trap 'rm -f midlertidig_fil.txt; echo "Rydder opp..."' EXIT
touch midlertidig_fil.txt
echo "Skriptet kjører. Fil opprettet."
sleep 5
```

### Eksempel 3: Håndtere flere signaler
Du kan også håndtere flere signaler med `trap`:

```sh
trap 'echo "Mottatt SIGTERM"; exit' SIGTERM
trap 'echo "Mottatt SIGINT"; exit' SIGINT
while true; do
    echo "Kjører skript... Trykk Ctrl+C eller send SIGTERM."
    sleep 1
done
```

## Tips
- Bruk `trap` for å sikre at skriptet alltid rydder opp etter seg, selv om det avbrytes.
- Test skriptet ditt med forskjellige signaler for å se hvordan det reagerer.
- Husk at `trap`-kommandoen kan brukes til å håndtere både brukerinitierte og systemgenererte signaler.