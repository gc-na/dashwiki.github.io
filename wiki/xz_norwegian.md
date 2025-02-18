# [Norsk] Debian Almquist Shell (dash) xz Bruk: Komprimere og dekomprimere filer

## Oversikt
`xz` er et kompresjonsverktøy som brukes til å komprimere og dekomprimere filer. Det benytter seg av LZMA-algoritmen, som gir høy kompresjonsgrad, noe som gjør det populært for lagring og distribusjon av data.

## Bruk
Grunnleggende syntaks for `xz`-kommandoen er som følger:

```
xz [alternativer] [argumenter]
```

## Vanlige alternativer
- `-d`, `--decompress`: Dekomprimerer en fil.
- `-k`, `--keep`: Bevarer den opprinnelige filen etter komprimering.
- `-f`, `--force`: Tvinger komprimering eller dekomprimering, selv om det kan overskrive eksisterende filer.
- `-9`: Angir maksimal kompresjon (kan være tregere).
- `-1` til `-9`: Angir kompresjonsnivå fra lav til høy.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `xz`:

### Komprimere en fil
For å komprimere en fil, kan du bruke følgende kommando:
```bash
xz fil.txt
```

### Dekomprimere en fil
For å dekomprimere en fil, kan du bruke:
```bash
xz -d fil.txt.xz
```

### Beholde den opprinnelige filen
Hvis du ønsker å beholde den opprinnelige filen etter komprimering, kan du bruke:
```bash
xz -k fil.txt
```

### Tvinge komprimering
For å tvinge komprimering og overskrive eksisterende filer, kan du bruke:
```bash
xz -f fil.txt
```

### Komprimere med maksimal kompresjon
For å oppnå maksimal kompresjon, kan du bruke:
```bash
xz -9 fil.txt
```

## Tips
- Vær oppmerksom på at komprimerte filer med `xz` får filendelsen `.xz`, så husk å sjekke filnavnene.
- Bruk `-k` alternativet hvis du er usikker på om du vil slette den opprinnelige filen.
- For batch-komprimering, kan du bruke jokertegn, som i `xz *.txt` for å komprimere alle tekstfiler i en katalog.