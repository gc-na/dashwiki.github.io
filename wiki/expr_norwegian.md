# [Norsk] Debian Almquist Shell (dash) expr Bruk: Utfør aritmetiske og logiske operasjoner

## Oversikt
`expr` er et kommandoverktøy i Debian Almquist Shell (dash) som brukes til å evaluere uttrykk og utføre aritmetiske og logiske operasjoner. Det kan håndtere både heltall og strenger, og er nyttig for skripting og kommandolinjeoperasjoner.

## Bruk
Grunnleggende syntaks for `expr`-kommandoen er som følger:

```bash
expr [alternativer] [argumenter]
```

## Vanlige alternativer
- `+` : Legger sammen to tall.
- `-` : Trekker fra det andre tallet fra det første.
- `*` : Multipliserer to tall.
- `/` : Deler det første tallet med det andre.
- `%` : Beregner resten av divisjonen mellom to tall.
- `=` : Sjekker om to strenger er like.
- `!=` : Sjekker om to strenger ikke er like.
- `>` : Sjekker om den første strengen er større enn den andre.
- `<` : Sjekker om den første strengen er mindre enn den andre.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `expr` kan brukes:

### Aritmetiske operasjoner
Legge sammen to tall:

```bash
expr 5 + 3
```

Resultatet vil være `8`.

### Subtraksjon
Trekke fra to tall:

```bash
expr 10 - 4
```

Resultatet vil være `6`.

### Multiplikasjon
Multiplisere to tall:

```bash
expr 7 \* 6
```

Resultatet vil være `42`. (Merk at `*` må escapes med en backslash.)

### Divisjon
Dele to tall:

```bash
expr 20 / 4
```

Resultatet vil være `5`.

### Sammenligning av strenger
Sjekke om to strenger er like:

```bash
expr "hello" = "hello"
```

Resultatet vil være `1` (sann).

## Tips
- Husk å bruke backslash (`\`) foran spesialtegn som `*` for å unngå feil i kommandolinjen.
- `expr` returnerer `0` for falske uttrykk og `1` for sanne, noe som kan være nyttig i betingede uttrykk i skript.
- For mer komplekse operasjoner, vurder å bruke `awk` eller `bc`, da `expr` har begrensninger i forhold til flyttall og mer avanserte matematiske funksjoner.