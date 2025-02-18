# [Danish] Debian Almquist Shell (dash) find brug: Find filnavne

## Oversigt
`find`-kommandoen bruges til at søge efter filer og mapper i et filsystem baseret på forskellige kriterier som navn, type, størrelse og dato. Det er et kraftfuldt værktøj til at navigere i store mængder data.

## Brug
Den grundlæggende syntaks for `find`-kommandoen er som følger:

```bash
find [muligheder] [argumenter]
```

## Almindelige muligheder
- `-name`: Søg efter filer med et specifikt navn.
- `-type`: Angiv typen af filer, f.eks. `f` for almindelige filer og `d` for mapper.
- `-size`: Søg efter filer baseret på størrelse, f.eks. `+100M` for filer større end 100 MB.
- `-mtime`: Søg efter filer baseret på ændringsdato, f.eks. `-mtime -7` for filer ændret inden for de sidste 7 dage.
- `-exec`: Udfør en kommando på de fundne filer.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `find`-kommandoen kan bruges:

1. Søg efter en fil med et specifikt navn:
   ```bash
   find /sti/til/directory -name "filnavn.txt"
   ```

2. Søg efter alle mapper i et bestemt bibliotek:
   ```bash
   find /sti/til/directory -type d
   ```

3. Søg efter filer større end 50 MB:
   ```bash
   find /sti/til/directory -size +50M
   ```

4. Søg efter filer, der er ændret inden for de sidste 10 dage:
   ```bash
   find /sti/til/directory -mtime -10
   ```

5. Udfør en kommando på de fundne filer, f.eks. slet dem:
   ```bash
   find /sti/til/directory -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Brug `-print` for at vise resultaterne, hvis det ikke er standard.
- Kombiner flere kriterier ved hjælp af `-and` og `-or` for mere komplekse søgninger.
- Vær forsigtig med `-exec`-muligheden, da den kan ændre eller slette filer. Test først med `-print` for at se, hvilke filer der vil blive påvirket.