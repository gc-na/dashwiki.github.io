# [Norsk] Debian Almquist Shell (dash) gunzip bruksanvisning: Dekomprimere gzip-filer

## Oversikt
`gunzip` er et kommandoverktøy som brukes til å dekomprimere filer som er komprimert med gzip-formatet. Det er en del av GNU-prosjektet og er ofte brukt i Unix-lignende operativsystemer for å håndtere komprimerte data.

## Bruk
Den grunnleggende syntaksen for `gunzip` er som følger:

```bash
gunzip [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Skriver den dekomprimerte filen til standard utdata i stedet for å erstatte den opprinnelige filen.
- `-f`: Tvinger dekomprimering, selv om det kan overskrive eksisterende filer.
- `-k`: Beholder den opprinnelige komprimerte filen etter dekomprimering.
- `-r`: Dekomprimerer filer rekursivt i kataloger.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `gunzip`:

1. Dekomprimere en enkelt fil:
   ```bash
   gunzip filnavn.gz
   ```

2. Dekomprimere en fil og beholde den opprinnelige:
   ```bash
   gunzip -k filnavn.gz
   ```

3. Dekomprimere flere filer samtidig:
   ```bash
   gunzip fil1.gz fil2.gz fil3.gz
   ```

4. Skrive den dekomprimerte filen til standard utdata:
   ```bash
   gunzip -c filnavn.gz > nyfil.txt
   ```

5. Dekomprimere alle gzip-filer i en katalog rekursivt:
   ```bash
   gunzip -r /sti/til/katalog/
   ```

## Tips
- Vær oppmerksom på at `gunzip` vil overskrive eksisterende filer uten advarsel hvis du bruker `-f` alternativet.
- Bruk `-k` alternativet hvis du vil beholde de opprinnelige komprimerte filene etter dekomprimering.
- For å se innholdet i en gzip-fil uten å dekomprimere den, kan du bruke `zcat`-kommandoen.