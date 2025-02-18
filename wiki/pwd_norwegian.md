# [Norsk] Debian Almquist Shell (dash) pwd Bruk: Vise gjeldende arbeidskatalog

## Oversikt
`pwd` (print working directory) er en kommando som brukes i Debian Almquist Shell (dash) for å vise den nåværende arbeidskatalogen i terminalen. Den gir deg den fullstendige stien til katalogen du befinner deg i.

## Bruk
Grunnleggende syntaks for kommandoen er:

```bash
pwd [alternativer]
```

## Vanlige alternativer
- `-L`: Viser den logiske stien til den nåværende arbeidskatalogen, som kan inkludere symboliske lenker.
- `-P`: Viser den fysiske stien til den nåværende arbeidskatalogen, som følger den faktiske strukturen på filsystemet.

## Vanlige eksempler
For å vise den nåværende arbeidskatalogen, kan du bruke:

```bash
pwd
```

For å vise den logiske stien:

```bash
pwd -L
```

For å vise den fysiske stien:

```bash
pwd -P
```

## Tips
- Bruk `pwd` før du navigerer til en annen katalog for å huske hvor du startet.
- Kombiner `pwd` med andre kommandoer, som `cd`, for å sikre at du alltid vet hvor du er i filsystemet.
- Hvis du jobber med skript, kan det være nyttig å lagre utdataene fra `pwd` i en variabel for senere bruk.