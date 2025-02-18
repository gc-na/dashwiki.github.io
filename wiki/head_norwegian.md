# [Norsk] Debian Almquist Shell (dash) head bruken: viser de første linjene i en fil

## Oversikt
`head`-kommandoen brukes til å vise de første linjene i en eller flere filer. Dette er nyttig for raskt å se innholdet i en fil uten å åpne hele filen, spesielt når filen er stor.

## Bruk
Den grunnleggende syntaksen for `head`-kommandoen er som følger:

```bash
head [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n [antall]`: Angir hvor mange linjer som skal vises fra starten av filen. Standard er 10 linjer.
- `-c [antall]`: Viser et spesifisert antall byte fra starten av filen.
- `-q`: Undertrykker filnavnene i utdataene når flere filer vises.
- `-v`: Viser filnavnene i utdataene, selv når det bare er én fil.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `head`-kommandoen:

1. Vise de første 10 linjene i en fil:
   ```bash
   head filnavn.txt
   ```

2. Vise de første 5 linjene i en fil:
   ```bash
   head -n 5 filnavn.txt
   ```

3. Vise de første 20 byte av en fil:
   ```bash
   head -c 20 filnavn.txt
   ```

4. Vise de første 10 linjene fra flere filer:
   ```bash
   head fil1.txt fil2.txt
   ```

5. Vise de første 10 linjene og inkludere filnavnene:
   ```bash
   head -v filnavn.txt
   ```

## Tips
- Bruk `head` i kombinasjon med andre kommandoer ved hjelp av rør (`|`) for å analysere utdata. For eksempel, for å se de første linjene av utdataene fra `grep`:
  ```bash
  grep "søkeord" filnavn.txt | head -n 5
  ```
- Når du arbeider med store loggfiler, kan `head` være en rask måte å få en oversikt over de nyeste oppføringene.
- Husk at `head` alltid viser linjene fra toppen av filen, så det er nyttig for å sjekke innholdet i filer der de nyeste oppføringene er plassert øverst.