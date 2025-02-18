# [Danish] Debian Almquist Shell (dash) comm kommando: Sammenlign linjer fra to filer

## Oversigt
Kommandoen `comm` bruges til at sammenligne to sorterede filer linje for linje. Den viser forskellene og lighederne mellem filerne, hvilket gør det nemt at identificere unikke og fælles linjer.

## Brug
Den grundlæggende syntaks for `comm` er:

```bash
comm [muligheder] [argumenter]
```

## Almindelige muligheder
- `-1`: Undertrykker output af linjer, der kun findes i den første fil.
- `-2`: Undertrykker output af linjer, der kun findes i den anden fil.
- `-3`: Undertrykker output af linjer, der findes i begge filer.
- `-i`: Ignorerer forskelle i store og små bogstaver.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `comm`:

1. Sammenlign to filer og vis alle linjer:
   ```bash
   comm fil1.txt fil2.txt
   ```

2. Vis kun linjer, der findes i den første fil:
   ```bash
   comm -13 fil1.txt fil2.txt
   ```

3. Vis kun linjer, der findes i den anden fil:
   ```bash
   comm -12 fil1.txt fil2.txt
   ```

4. Ignorer forskelle i store og små bogstaver:
   ```bash
   comm -i fil1.txt fil2.txt
   ```

## Tips
- Sørg for, at filerne er sorteret, før du bruger `comm`, da kommandoen kun fungerer korrekt med sorterede filer.
- Brug `sort`-kommandoen til at sortere filerne, hvis de ikke allerede er det:
  ```bash
  sort fil1.txt -o fil1.txt
  sort fil2.txt -o fil2.txt
  ```
- Kombiner `comm` med andre kommandoer som `grep` for at filtrere resultaterne yderligere.