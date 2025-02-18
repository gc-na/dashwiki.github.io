# [Norsk] Debian Almquist Shell (dash) tr: [endre tegn]

## Oversikt
`tr` er et kommandolinjeverktøy som brukes til å oversette eller slette tegn i tekst. Det er nyttig for å manipulere tekststrenger, for eksempel ved å erstatte spesifikke tegn eller fjerne uønskede tegn.

## Bruk
Den grunnleggende syntaksen for `tr` er som følger:

```bash
tr [alternativer] [argumenter]
```

## Vanlige alternativer
- `-d`: Sletter de angitte tegnene fra input.
- `-s`: Komprimerer påfølgende forekomster av tegn til ett enkelt tegn.
- `-c`: Angir komplementet av de angitte tegnene, dvs. alle tegn som ikke er spesifisert.

## Vanlige eksempler

### Erstatte tegn
For å erstatte alle små bokstaver med store bokstaver:

```bash
echo "hei verden" | tr 'a-z' 'A-Z'
```

### Slette tegn
For å fjerne alle tall fra en tekst:

```bash
echo "abc123def456" | tr -d '0-9'
```

### Komprimere tegn
For å komprimere påfølgende mellomrom til ett enkelt mellomrom:

```bash
echo "Dette   er   en   test" | tr -s ' '
```

### Bruke komplement
For å erstatte alle tegn som ikke er vokaler med et stjernesymbol:

```bash
echo "Hei på deg" | tr -c 'aeiouAEIOU' '*'
```

## Tips
- Bruk `echo` for å teste `tr`-kommandoer raskt før du bruker dem på filer.
- Kombiner `tr` med andre kommandoer som `grep` eller `sed` for mer avansert tekstbehandling.
- Vær oppmerksom på at `tr` arbeider med enkelttegn og ikke med strenger, så det er viktig å spesifisere tegnene nøyaktig.