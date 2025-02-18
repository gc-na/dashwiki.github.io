# [Danish] Debian Almquist Shell (dash) xz brug: Komprimering og dekomprimering af filer

## Oversigt
`xz` er et kommandolinjeværktøj, der bruges til at komprimere og dekomprimere filer ved hjælp af LZMA-algoritmen. Det er kendt for at give høj komprimeringsgrad, hvilket gør det ideelt til at reducere filstørrelser.

## Brug
Den grundlæggende syntaks for `xz`-kommandoen er:

```bash
xz [muligheder] [argumenter]
```

## Almindelige muligheder
- `-d`, `--decompress`: Dekomprimerer en fil.
- `-k`, `--keep`: Beholder den originale fil efter komprimering.
- `-f`, `--force`: Tvinger komprimering eller dekomprimering, selvom det kan overskrive eksisterende filer.
- `-z`, `--compress`: Komprimerer en fil (standardindstillingen).
- `-9`: Angiver den højeste komprimeringsgrad.

## Almindelige eksempler
For at komprimere en fil ved navn `eksempel.txt` kan du bruge:

```bash
xz eksempel.txt
```

For at dekomprimere en fil ved navn `eksempel.txt.xz`:

```bash
xz -d eksempel.txt.xz
```

Hvis du vil komprimere en fil og samtidig beholde den originale fil, kan du gøre det med:

```bash
xz -k eksempel.txt
```

For at tvinge komprimering af en fil, selvom der allerede findes en komprimeret version:

```bash
xz -f eksempel.txt
```

## Tips
- Brug `-9` for at opnå maksimal komprimering, men vær opmærksom på, at det kan tage længere tid.
- Overvej at bruge `-k` for at undgå at miste den originale fil, indtil du er sikker på, at komprimeringen er vellykket.
- Tjek komprimeringsresultaterne ved at sammenligne filstørrelserne før og efter komprimering for at sikre, at du opnår den ønskede reduktion.