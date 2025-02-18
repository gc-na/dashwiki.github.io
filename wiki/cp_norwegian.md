# [Norsk] Debian Almquist Shell (dash) cp Bruk: Kopier filer og kataloger

## Oversikt
`cp`-kommandoen brukes til å kopiere filer og kataloger fra ett sted til et annet i Unix-lignende operativsystemer, inkludert Debian Almquist Shell (dash). Den lar brukeren lage kopier av filer og kataloger, noe som er nyttig for sikkerhetskopiering og organisering av data.

## Bruk
Grunnleggende syntaks for `cp`-kommandoen er som følger:

```sh
cp [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-r`: Kopierer kataloger rekursivt.
- `-i`: Spør om bekreftelse før overskrivning av eksisterende filer.
- `-u`: Kopierer bare filer som er nyere enn de eksisterende filene i målplasseringen.
- `-v`: Viser detaljer om hva som blir kopiert (verbose).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `cp`-kommandoen kan brukes:

1. Kopiere en fil til en annen plassering:
   ```sh
   cp fil.txt /sti/til/mål/
   ```

2. Kopiere en katalog og alt innholdet i den:
   ```sh
   cp -r katalog /sti/til/mål/
   ```

3. Kopiere en fil og spørre om bekreftelse før overskrivning:
   ```sh
   cp -i fil.txt /sti/til/mål/
   ```

4. Kopiere en fil bare hvis den er nyere enn den eksisterende filen i mål:
   ```sh
   cp -u fil.txt /sti/til/mål/
   ```

5. Vise detaljer om kopieringen:
   ```sh
   cp -v fil.txt /sti/til/mål/
   ```

## Tips
- Bruk `-i`-alternativet for å unngå utilsiktet overskrivning av filer.
- Når du kopierer kataloger, husk alltid å bruke `-r` for å inkludere alle underkataloger og filer.
- Sjekk alltid målplasseringen etter kopiering for å bekrefte at filene er kopiert som forventet.