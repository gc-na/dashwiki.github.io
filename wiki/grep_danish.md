# [Danish] Debian Almquist Shell (dash) grep brug: Søg i tekst

## Overview
`grep` er et kommandolinjeværktøj, der bruges til at søge efter specifikke mønstre i tekstfiler. Det står for "Global Regular Expression Print" og er meget nyttigt til at finde linjer, der matcher et givet mønster.

## Usage
Den grundlæggende syntaks for `grep` er som følger:

```bash
grep [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `grep`:

- `-i`: Ignorerer store og små bogstaver under søgningen.
- `-v`: Viser linjer, der ikke matcher mønsteret.
- `-r`: Søger rekursivt i alle filer i en mappe.
- `-n`: Viser linjenumre for de fundne match.
- `-l`: Viser kun filnavne, der indeholder et match.

## Common Examples
Her er nogle praktiske eksempler på, hvordan `grep` kan bruges:

1. Søg efter et ord i en fil:
   ```bash
   grep "ord" filnavn.txt
   ```

2. Ignorer store og små bogstaver under søgningen:
   ```bash
   grep -i "ord" filnavn.txt
   ```

3. Vis linjer, der ikke indeholder et bestemt ord:
   ```bash
   grep -v "ord" filnavn.txt
   ```

4. Søg rekursivt i en mappe:
   ```bash
   grep -r "ord" /sti/til/mappe
   ```

5. Vis linjenumre for de fundne match:
   ```bash
   grep -n "ord" filnavn.txt
   ```

## Tips
- Brug `grep` sammen med andre kommandoer ved hjælp af pipe (`|`) for at filtrere output. For eksempel:
  ```bash
  dmesg | grep "fejl"
  ```
- For at søge i flere filer, kan du bruge jokertegn:
  ```bash
  grep "ord" *.txt
  ```
- Overvej at bruge `--color` for at fremhæve de fundne match i output:
  ```bash
  grep --color "ord" filnavn.txt
  ```