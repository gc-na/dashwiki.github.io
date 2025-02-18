# [Norsk] Debian Almquist Shell (dash) comm: Sammenligne sorterte filer linje for linje

## Oversikt
`comm`-kommandoen brukes til å sammenligne to sorterte filer linje for linje. Den viser hvilke linjer som er unike for hver fil, samt linjer som er felles for begge filer. Dette er nyttig for å identifisere forskjeller og likheter mellom to datasett.

## Bruk
Den grunnleggende syntaksen for `comm`-kommandoen er som følger:
```bash
comm [alternativer] [fil1] [fil2]
```

## Vanlige alternativer
- `-1`: Undertrykk linjer som bare finnes i den første filen.
- `-2`: Undertrykk linjer som bare finnes i den andre filen.
- `-3`: Undertrykk linjer som finnes i begge filer.
- `-i`: Ignorer forskjeller mellom store og små bokstaver.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `comm`:

1. Sammenligne to filer og vise alle linjer:
   ```bash
   comm fil1.txt fil2.txt
   ```

2. Vise linjer som kun finnes i den første filen:
   ```bash
   comm -13 fil1.txt fil2.txt
   ```

3. Vise linjer som kun finnes i den andre filen:
   ```bash
   comm -12 fil1.txt fil2.txt
   ```

4. Sammenligne to filer uten å ta hensyn til store og små bokstaver:
   ```bash
   comm -i fil1.txt fil2.txt
   ```

## Tips
- Sørg for at filene du sammenligner er sortert, ellers kan resultatene bli uventede.
- Du kan bruke `sort`-kommandoen før `comm` for å sortere filene automatisk:
  ```bash
  comm <(sort fil1.txt) <(sort fil2.txt)
  ```
- Bruk `-` som filnavn for å lese fra standard input, noe som kan være nyttig i skript.