# [Danish] Debian Almquist Shell (dash) bunzip2 brug: Dekomprimere bzip2-filer

## Oversigt
`bunzip2` er et kommandolinjeværktøj, der bruges til at dekomprimere filer, der er komprimeret med bzip2-algoritmen. Det er en del af bzip2-pakken og er nyttigt til at reducere filstørrelser for effektiv lagring og overførsel.

## Brug
Den grundlæggende syntaks for `bunzip2`-kommandoen er:

```bash
bunzip2 [muligheder] [argumenter]
```

## Almindelige muligheder
- `-k`: Behold den komprimerede fil efter dekomprimering.
- `-f`: Tving dekomprimering, selvom der er en eksisterende fil med samme navn.
- `-v`: Vis detaljeret output om dekomprimeringsprocessen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `bunzip2`:

1. Dekomprimere en bzip2-fil:
   ```bash
   bunzip2 fil.bz2
   ```

2. Dekomprimere en bzip2-fil og bevare den originale fil:
   ```bash
   bunzip2 -k fil.bz2
   ```

3. Tvinge dekomprimering, hvis filen allerede findes:
   ```bash
   bunzip2 -f fil.bz2
   ```

4. Dekomprimere en fil og vise detaljeret output:
   ```bash
   bunzip2 -v fil.bz2
   ```

## Tips
- Sørg for at have tilstrækkelig diskplads, da dekomprimering kan kræve mere plads end den komprimerede fil.
- Brug `-k` muligheden, hvis du ønsker at bevare den originale komprimerede fil til senere brug.
- Tjek filens integritet efter dekomprimering for at sikre, at den ikke er blevet beskadiget under processen.