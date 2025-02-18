# [Danish] Debian Almquist Shell (dash) dstat brug: overvågning af systemressourcer

## Oversigt
dstat er et værktøj til realtids overvågning af systemressourcer, der kombinerer funktionerne fra flere andre værktøjer som vmstat, iostat og netstat. Det giver en omfattende oversigt over systemets ydeevne, hvilket gør det nemt at identificere flaskehalse og overvåge systemets tilstand.

## Brug
Den grundlæggende syntaks for dstat er:

```bash
dstat [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c`: Vis CPU-brug.
- `-d`: Vis diskaktivitet.
- `-n`: Vis netværksaktivitet.
- `-m`: Vis hukommelsesbrug.
- `--help`: Vis hjælp og tilgængelige muligheder.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge dstat:

1. **Vis CPU og diskaktivitet:**
   ```bash
   dstat -c -d
   ```

2. **Vis netværks- og hukommelsesbrug:**
   ```bash
   dstat -n -m
   ```

3. **Vis alle ressourcer i realtid:**
   ```bash
   dstat
   ```

4. **Gem output til en fil:**
   ```bash
   dstat > dstat_output.txt
   ```

## Tips
- Brug dstat med `--help` for at få en liste over alle tilgængelige muligheder.
- Overvej at køre dstat i baggrunden, hvis du ønsker at overvåge systemet i længere tid.
- Kombiner dstat med andre værktøjer som grep for at filtrere output og fokusere på specifikke data.