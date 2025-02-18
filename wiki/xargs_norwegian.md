# [Norsk] Debian Almquist Shell (dash) xargs bruk: Behandle standard input

## Oversikt
`xargs` er et kommandolinjeverktøy som brukes til å bygge og kjøre kommandoer fra standard input. Det tar data fra standard input og konverterer dem til argumenter for en annen kommando. Dette er spesielt nyttig når du har mange filer eller data som du ønsker å prosessere med en enkelt kommando.

## Bruk
Den grunnleggende syntaksen for `xargs` er som følger:

```
xargs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n N`: Angir hvor mange argumenter som skal sendes til kommandoen per gang.
- `-d DELIM`: Angir en spesifikk avgrenser for input i stedet for standard ny linje.
- `-0`: Behandler input som null-terminerte strenger, nyttig for filer med mellomrom i navnet.
- `-p`: Spør brukeren om bekreftelse før hver kommando kjøres.

## Vanlige eksempler

### Eksempel 1: Slette filer
For å slette alle `.tmp`-filer i den nåværende katalogen, kan du bruke:

```bash
find . -name "*.tmp" | xargs rm
```

### Eksempel 2: Kopiere filer
Kopiere alle `.jpg`-filer fra en katalog til en annen:

```bash
find /source/directory -name "*.jpg" | xargs -I {} cp {} /destination/directory
```

### Eksempel 3: Lese fra en fil
Hvis du har en fil som inneholder en liste over filnavn, kan du bruke `xargs` til å prosessere dem:

```bash
cat filelist.txt | xargs -n 1 echo
```

### Eksempel 4: Bruke null-terminerte strenger
For å håndtere filer med mellomrom i navnet, kan du bruke `-0` sammen med `find`:

```bash
find . -name "*.txt" -print0 | xargs -0 rm
```

## Tips
- Bruk `-n` for å begrense antall argumenter som sendes til kommandoen for å unngå feil ved for mange argumenter.
- Kombiner `xargs` med `find` for effektiv filbehandling.
- Vær oppmerksom på spesialtegn og mellomrom i filnavn; bruk `-0` for å unngå problemer.
- Test alltid kommandoene dine med `echo` før du kjører dem for å se hva som vil bli utført.