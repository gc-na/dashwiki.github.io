# [Norsk] Debian Almquist Shell (dash) find bruken: Finn filnavn

## Oversikt
`find`-kommandoen brukes til å søke etter filer og kataloger i et filsystem. Den kan søke basert på forskjellige kriterier som navn, type, størrelse, og mer. Dette gjør det til et kraftig verktøy for filhåndtering.

## Bruk
Den grunnleggende syntaksen for `find`-kommandoen er:

```
find [alternativer] [argumenter]
```

## Vanlige alternativer
- `-name`: Søk etter filer med et spesifikt navn.
- `-type`: Filtrer søkeresultater basert på filtype (f.eks. `f` for vanlige filer, `d` for kataloger).
- `-size`: Søk etter filer basert på størrelse (f.eks. `+100k` for filer større enn 100 kilobyte).
- `-mtime`: Søk etter filer basert på endringsdato (f.eks. `-mtime -7` for filer endret de siste 7 dagene).
- `-exec`: Kjør en kommando på hver fil som blir funnet.

## Vanlige eksempler

### Søk etter en fil med et spesifikt navn
```bash
find /path/to/search -name "filnavn.txt"
```

### Søk etter alle kataloger
```bash
find /path/to/search -type d
```

### Søk etter filer større enn 1 MB
```bash
find /path/to/search -size +1M
```

### Søk etter filer endret de siste 30 dagene
```bash
find /path/to/search -mtime -30
```

### Kjør en kommando på hver fil som blir funnet
```bash
find /path/to/search -name "*.log" -exec rm {} \;
```

## Tips
- Bruk `-print` for å vise resultatene i terminalen hvis du bruker `-exec`.
- Kombiner alternativer for mer presise søk, for eksempel `find /path -type f -name "*.txt" -size +1M`.
- Vær forsiktig med `-exec`-alternativet, spesielt når du sletter filer, for å unngå utilsiktet datatap.