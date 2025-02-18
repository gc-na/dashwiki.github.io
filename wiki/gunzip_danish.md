# [Danish] Debian Almquist Shell (dash) gunzip brug: Dekomprimere gzip-filer

## Oversigt
`gunzip` er et kommandolinjeværktøj, der bruges til at dekomprimere filer, der er komprimeret med gzip-formatet. Det fjerner komprimeringen og gendanner den oprindelige fil.

## Brug
Den grundlæggende syntaks for `gunzip`-kommandoen er:

```bash
gunzip [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c`: Skriver den dekomprimerede output til standard output (stdout) i stedet for at overskrive filen.
- `-f`: Tvinger dekomprimering, selvom der allerede findes en fil med samme navn.
- `-k`: Beholder den komprimerede fil efter dekomprimering.
- `-r`: Dekomprimerer filer rekursivt i de angivne mapper.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `gunzip`:

1. Dekomprimere en enkelt fil:
   ```bash
   gunzip filnavn.gz
   ```

2. Dekomprimere en fil og beholde den komprimerede version:
   ```bash
   gunzip -k filnavn.gz
   ```

3. Dekomprimere flere filer på én gang:
   ```bash
   gunzip fil1.gz fil2.gz fil3.gz
   ```

4. Dekomprimere en fil og skrive output til standard output:
   ```bash
   gunzip -c filnavn.gz > outputfil
   ```

5. Dekomprimere filer rekursivt i en mappe:
   ```bash
   gunzip -r /sti/til/mappe
   ```

## Tips
- Sørg for at have en sikkerhedskopi af dine filer, før du bruger `gunzip`, især når du bruger `-f`-muligheden.
- Brug `-k`-muligheden, hvis du vil beholde den komprimerede fil til senere brug.
- Hvis du arbejder med mange filer, kan det være nyttigt at bruge `-r`-muligheden for at spare tid.