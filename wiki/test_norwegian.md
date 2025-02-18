# [Norsk] Debian Almquist Shell (dash) test bruk: Sjekke betingelser

## Oversikt
`test`-kommandoen brukes i Debian Almquist Shell (dash) for å evaluere betingelser og returnere en statuskode basert på resultatet. Den er nyttig for skripting og kan brukes til å sjekke filattributter, sammenligne verdier og mer.

## Bruk
Grunnleggende syntaks for `test`-kommandoen er som følger:

```sh
test [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e`: Sjekker om en fil eksisterer.
- `-f`: Sjekker om en fil er en vanlig fil.
- `-d`: Sjekker om en fil er en katalog.
- `-z`: Sjekker om lengden på en streng er null.
- `=`: Sjekker om to strenger er like.
- `-ne`: Sjekker om to tall ikke er like.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `test`-kommandoen kan brukes:

### Sjekke om en fil eksisterer
```sh
test -e fil.txt && echo "Fil eksisterer"
```

### Sjekke om en fil er en vanlig fil
```sh
test -f fil.txt && echo "Dette er en vanlig fil"
```

### Sjekke om en katalog eksisterer
```sh
test -d /path/to/directory && echo "Katalogen eksisterer"
```

### Sjekke om en streng er tom
```sh
str=" "
test -z "$str" && echo "Strengen er tom"
```

### Sammenligne to strenger
```sh
str1="hei"
str2="hei"
test "$str1" = "$str2" && echo "Strengene er like"
```

### Sammenligne to tall
```sh
tall1=5
tall2=10
test $tall1 -ne $tall2 && echo "Tallene er ikke like"
```

## Tips
- Bruk `[` som en alternativ syntaks for `test`, for eksempel: `[ -e fil.txt ]`.
- Husk at `test` returnerer en statuskode, der 0 betyr "sann" og 1 betyr "usann".
- For mer lesbarhet, vurder å bruke `&&` og `||` for å kjede sammen flere betingelser og handlinger.