# [Norsk] Debian Almquist Shell (dash) cd bruken: Navigere i kataloger

## Oversikt
`cd`-kommandoen brukes til å endre den nåværende arbeidskatalogen i Debian Almquist Shell (dash). Dette gjør det mulig for brukeren å navigere mellom forskjellige kataloger i filsystemet.

## Bruk
Grunnleggende syntaks for `cd`-kommandoen er som følger:

```bash
cd [alternativer] [argumenter]
```

## Vanlige alternativer
- `-`: Går tilbake til den forrige katalogen.
- `..`: Går opp ett nivå i katalogstrukturen.
- `~`: Går til brukerens hjemmekatalog.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `cd`-kommandoen brukes:

### Gå til hjemmekatalogen
```bash
cd ~
```

### Gå opp ett nivå i katalogstrukturen
```bash
cd ..
```

### Gå til en spesifikk katalog
```bash
cd /path/to/directory
```

### Gå tilbake til forrige katalog
```bash
cd -
```

## Tips
- Bruk `cd` med `Tab`-tasten for automatisk fullføring av katalognavn.
- Sjekk alltid den nåværende katalogen ved å bruke `pwd` etter å ha endret katalog.
- Unngå å bruke relative stier hvis du jobber med skript, da det kan føre til forvirring om den nåværende katalogen.