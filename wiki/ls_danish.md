# [Danish] Debian Almquist Shell (dash) ls brug: Vis indholdet af en mappe

## Overview
`ls` kommandoen bruges til at liste indholdet af en mappe i Unix-lignende operativsystemer. Den viser filer og undermapper i den angivne katalog, hvilket gør det nemt at se, hvad der er tilgængeligt.

## Usage
Den grundlæggende syntaks for `ls` kommandoen er som følger:

```bash
ls [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `ls`:

- `-l`: Viser en detaljeret liste med oplysninger om filer og mapper.
- `-a`: Viser alle filer, inklusive skjulte filer, der begynder med punktum.
- `-h`: Viser filstørrelser i et læsbart format (f.eks. KB, MB).
- `-R`: Viser indholdet af undermapper rekursivt.
- `-t`: Sorterer filer efter ændringsdato.

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `ls`:

1. For at liste indholdet af den nuværende mappe:
   ```bash
   ls
   ```

2. For at vise en detaljeret liste over filer og mapper:
   ```bash
   ls -l
   ```

3. For at inkludere skjulte filer i listen:
   ```bash
   ls -a
   ```

4. For at vise filstørrelser i et læsbart format:
   ```bash
   ls -lh
   ```

5. For at vise indholdet af undermapper rekursivt:
   ```bash
   ls -R
   ```

## Tips
- Brug `ls -la` for at få en omfattende oversigt over alle filer, inklusive skjulte.
- Kombiner muligheder for at tilpasse output, f.eks. `ls -lt` for at sortere filer efter dato.
- Overvej at bruge aliaser i din shell-konfiguration for at gøre det lettere at bruge `ls` med dine foretrukne indstillinger.