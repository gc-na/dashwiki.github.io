# [Danish] Debian Almquist Shell (dash) gzip brug: Komprimering af filer

## Oversigt
`gzip` er et kommandolinjeværktøj, der bruges til at komprimere filer. Det reducerer filstørrelsen ved at anvende Lempel-Ziv algoritmen, hvilket gør det ideelt til at spare plads og båndbredde ved overførsel af data.

## Brug
Den grundlæggende syntaks for `gzip`-kommandoen er som følger:

```bash
gzip [muligheder] [argumenter]
```

## Almindelige muligheder
- `-d` : Dekomprimerer en gzip-komprimeret fil.
- `-k` : Bevarer den originale fil efter komprimering.
- `-v` : Viser detaljeret output om komprimeringsprocessen.
- `-f` : Tvinger komprimering, selv hvis der allerede findes en fil med samme navn.
- `-r` : Komprimerer filer rekursivt i en mappe.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `gzip`:

1. Komprimere en fil:
   ```bash
   gzip fil.txt
   ```

2. Dekomprimere en gzip-fil:
   ```bash
   gzip -d fil.txt.gz
   ```

3. Bevare den originale fil under komprimering:
   ```bash
   gzip -k fil.txt
   ```

4. Vise detaljer under komprimering:
   ```bash
   gzip -v fil.txt
   ```

5. Komprimere alle `.txt`-filer i en mappe rekursivt:
   ```bash
   gzip -r *.txt
   ```

## Tips
- Overvej at bruge `-k` muligheden, hvis du vil beholde den originale fil, mens du komprimerer.
- Brug `-v` for at få indsigt i, hvor meget plads du sparer ved komprimering.
- For batch-komprimering, kan du bruge jokertegn som `*` til at komprimere flere filer på én gang.