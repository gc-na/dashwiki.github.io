# [Danish] Debian Almquist Shell (dash) bzip2 Brug: Komprimering af filer

## Oversigt
bzip2 er et kommandolinjeværktøj, der bruges til at komprimere filer ved hjælp af Burrows-Wheeler-algoritmen. Det skaber en .bz2-fil, som er betydeligt mindre end den originale fil, hvilket sparer plads og gør det lettere at overføre data.

## Brug
Den grundlæggende syntaks for bzip2-kommandoen er:

```
bzip2 [muligheder] [argumenter]
```

## Almindelige muligheder
- `-d`, `--decompress`: Dekomprimerer en .bz2-fil.
- `-k`, `--keep`: Bevarer den originale fil efter komprimering.
- `-f`, `--force`: Tvinger komprimering, selvom outputfilen allerede eksisterer.
- `-v`, `--verbose`: Viser detaljer om komprimeringsprocessen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger bzip2:

1. **Komprimere en fil**:
   ```bash
   bzip2 fil.txt
   ```
   Dette vil komprimere `fil.txt` til `fil.txt.bz2`.

2. **Dekomprimere en .bz2-fil**:
   ```bash
   bzip2 -d fil.txt.bz2
   ```
   Dette vil gendanne den originale `fil.txt` fra `fil.txt.bz2`.

3. **Bevare den originale fil under komprimering**:
   ```bash
   bzip2 -k fil.txt
   ```
   Dette vil komprimere `fil.txt` til `fil.txt.bz2` og samtidig bevare den originale `fil.txt`.

4. **Tvinge komprimering**:
   ```bash
   bzip2 -f fil.txt
   ```
   Hvis `fil.txt.bz2` allerede eksisterer, vil denne kommando overskrive den.

5. **Vis detaljer om komprimeringsprocessen**:
   ```bash
   bzip2 -v fil.txt
   ```
   Dette vil vise information om komprimeringsprocessen, herunder komprimeringsforholdet.

## Tips
- Brug `-k` muligheden, hvis du ønsker at beholde den originale fil, mens du komprimerer.
- Vær opmærksom på, at bzip2 kan være langsommere end andre komprimeringsværktøjer som gzip, men det giver ofte bedre komprimeringsforhold.
- For at komprimere flere filer på én gang, kan du bruge en wildcard, som f.eks. `bzip2 *.txt` for at komprimere alle tekstfiler i den aktuelle mappe.