# [Norsk] Debian Almquist Shell (dash) cmp Bruk: Sammenlign filer byte-for-byte

## Oversikt
`cmp`-kommandoen brukes til å sammenligne to filer byte-for-byte. Den viser hvor de første forskjellene mellom filene finnes, og kan være nyttig for å sjekke om to filer er identiske eller for å finne ut hvor de avviker.

## Bruk
Den grunnleggende syntaksen for `cmp`-kommandoen er:

```sh
cmp [alternativer] [fil1] [fil2]
```

## Vanlige alternativer
- `-l`: List opp alle byte som er forskjellige, sammen med deres posisjoner.
- `-s`: Still stille; ingen utdata, men returnerer en statuskode som indikerer om filene er like eller forskjellige.
- `-i OFFSET`: Start sammenligningen fra en spesifisert byte-offset.
- `-n N`: Sammenlign bare de første N byte av filene.

## Vanlige eksempler
Sammenlign to filer og vis den første forskjellen:

```sh
cmp fil1.txt fil2.txt
```

Bruk `-l` for å liste opp alle forskjeller:

```sh
cmp -l fil1.txt fil2.txt
```

Sjekk om to filer er like uten å vise utdata:

```sh
cmp -s fil1.txt fil2.txt
```

Sammenlign bare de første 10 byte av to filer:

```sh
cmp -n 10 fil1.txt fil2.txt
```

## Tips
- Bruk `cmp` når du trenger en rask og effektiv måte å sammenligne filer på, spesielt store filer.
- Kombiner `cmp` med andre kommandoer som `grep` for mer avansert filtrering av utdata.
- Husk at `cmp` er sensitiv for filtyper; det kan være nyttig å bruke det på binære filer så vel som tekstfiler.