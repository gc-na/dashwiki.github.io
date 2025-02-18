# [Dansk] Debian Almquist Shell (dash) sort brug: Sortering af linjer i tekstfiler

## Oversigt
`sort`-kommandoen bruges til at sortere linjer i tekstfiler. Den kan håndtere både standard input og filer, hvilket gør den nyttig til at organisere data i en ønsket rækkefølge.

## Brug
Den grundlæggende syntaks for `sort`-kommandoen er:

```bash
sort [muligheder] [argumenter]
```

## Almindelige muligheder
- `-r`: Sorter i omvendt rækkefølge.
- `-n`: Sorter numerisk i stedet for alfabetisk.
- `-k`: Angiv hvilken kolonne der skal sorteres efter.
- `-u`: Fjern dubletter fra output.
- `-o`: Angiv en fil til at gemme det sorterede output.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `sort`:

1. **Sortering af en fil alfabetisk:**
   ```bash
   sort fil.txt
   ```

2. **Sortering af en fil i omvendt rækkefølge:**
   ```bash
   sort -r fil.txt
   ```

3. **Sortering af tal i en fil:**
   ```bash
   sort -n tal.txt
   ```

4. **Sortering efter en specifik kolonne:**
   ```bash
   sort -k 2 fil.txt
   ```

5. **Fjernelse af dubletter fra sorteret output:**
   ```bash
   sort -u fil.txt
   ```

6. **Gem det sorterede output i en ny fil:**
   ```bash
   sort fil.txt -o sorterede_fil.txt
   ```

## Tips
- Brug `-n` når du sorterer tal for at sikre, at de bliver sorteret korrekt.
- Kombiner `-k` og `-r` for at sortere efter specifikke kolonner i omvendt rækkefølge.
- Tjek indholdet af filen med `cat` før sortering for at forstå, hvordan dataene er struktureret.