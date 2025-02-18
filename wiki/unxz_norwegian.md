# [Norsk] Debian Almquist Shell (dash) unxz bruksanvisning: Dekomprimere .xz-filer

## Oversikt
`unxz` er et kommandoverktøy som brukes til å dekomprimere filer som er komprimert med XZ-formatet. Det fjerner komprimeringen fra .xz-filer og gjenoppretter den opprinnelige filen.

## Bruk
Den grunnleggende syntaksen for `unxz`-kommandoen er som følger:

```
unxz [alternativer] [argumenter]
```

## Vanlige alternativer
- `-k`, `--keep`: Behold den opprinnelige komprimerte filen etter dekomprimering.
- `-f`, `--force`: Tving dekomprimering, selv om det kan overskrive eksisterende filer.
- `-v`, `--verbose`: Vis detaljer om prosessen under dekomprimering.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du bruker `unxz`:

1. Dekomprimere en enkelt .xz-fil:
   ```bash
   unxz filnavn.xz
   ```

2. Dekomprimere en .xz-fil og beholde den opprinnelige filen:
   ```bash
   unxz -k filnavn.xz
   ```

3. Tvinge dekomprimering av en fil, selv om det kan overskrive eksisterende filer:
   ```bash
   unxz -f filnavn.xz
   ```

4. Dekomprimere en fil og vise detaljer om prosessen:
   ```bash
   unxz -v filnavn.xz
   ```

## Tips
- Sørg for å ha en sikkerhetskopi av viktige filer før du bruker `-f`-alternativet, da det kan overskrive eksisterende filer.
- Bruk `-k`-alternativet hvis du vil beholde den komprimerte filen for fremtidig bruk.
- For batch-dekomprimering av flere filer, kan du bruke jokertegn:
  ```bash
  unxz *.xz
  ```