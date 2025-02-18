# [Norsk] Debian Almquist Shell (dash) brukere: [liste over brukere]

## Oversikt
`users`-kommandoen viser en liste over brukere som for øyeblikket er pålogget systemet. Den gir en enkel måte å se hvem som er aktive på systemet, noe som kan være nyttig for systemadministrasjon og overvåking.

## Bruk
Den grunnleggende syntaksen for `users`-kommandoen er:

```bash
users [alternativer]
```

## Vanlige alternativer
`users`-kommandoen har ikke mange alternativer, men her er noen nyttige:

- `-u`: Viser brukernavnene i en mer detaljert format, inkludert tilleggsinformasjon om hver bruker.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `users`-kommandoen:

1. For å vise en liste over alle påloggede brukere:

    ```bash
    users
    ```

2. For å vise brukerne med tilleggsinformasjon:

    ```bash
    users -u
    ```

## Tips
- Bruk `who`-kommandoen i tillegg til `users` for mer detaljert informasjon om påloggede brukere, inkludert tidspunkt for innlogging og terminalinformasjon.
- Kombiner `users` med `wc -w` for å telle antall påloggede brukere:

    ```bash
    users | wc -w
    ```

- Husk at `users` bare viser brukere som er pålogget, så hvis ingen er pålogget, vil kommandoen returnere en tom linje.