# [Norsk] Debian Almquist Shell (dash) free: Vis minnebruk

## Oversikt
`free`-kommandoen brukes til å vise informasjon om minnebruk på systemet. Den gir en oversikt over tilgjengelig, brukt og buffret minne, noe som er nyttig for systemadministrasjon og ytelsesanalyse.

## Bruk
Den grunnleggende syntaksen for `free`-kommandoen er som følger:

```bash
free [alternativer]
```

## Vanlige alternativer
- `-h`: Viser minneverdier i et lesbart format (f.eks. MB eller GB).
- `-m`: Viser minneverdier i megabyte.
- `-g`: Viser minneverdier i gigabyte.
- `-s [sekunder]`: Oppdaterer visningen med angitt intervall i sekunder.
- `-t`: Viser total minnebruk, inkludert swap-minne.

## Vanlige eksempler
For å vise minnebruk i et lesbart format:

```bash
free -h
```

For å vise minneverdier i megabyte:

```bash
free -m
```

For å vise minnebruk med oppdatering hvert 5. sekund:

```bash
free -s 5
```

For å inkludere total minnebruk:

```bash
free -h -t
```

## Tips
- Bruk `-h` for å få en enklere lesbar utdata, spesielt på systemer med mye minne.
- Kombiner `free` med andre kommandoer som `watch` for å overvåke minnebruk i sanntid:
  
  ```bash
  watch free -h
  ```
- Sjekk minnebruken regelmessig for å sikre at systemet ditt fungerer optimalt, spesielt før og etter installasjon av nye programmer.