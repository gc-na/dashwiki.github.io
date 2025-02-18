# [Norsk] Debian Almquist Shell (dash) basename bruk: Få filnavn uten bane

## Oversikt
`basename`-kommandoen brukes til å hente filnavnet fra en full filbane. Dette er nyttig når du ønsker å isolere selve filnavnet fra stien som leder til det.

## Bruk
Den grunnleggende syntaksen for `basename`-kommandoen er som følger:

```
basename [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Behandle flere argumenter og returnere filnavnene for hver av dem.
- `-s, --suffix=SUFFIX`: Fjerner den angitte suffiksen fra filnavnet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `basename`:

1. Hente filnavnet fra en full bane:
   ```sh
   basename /path/to/file.txt
   ```
   Utdata: `file.txt`

2. Hente filnavnet uten suffiks:
   ```sh
   basename /path/to/file.txt .txt
   ```
   Utdata: `file`

3. Behandle flere filer samtidig:
   ```sh
   basename -a /path/to/file1.txt /path/to/file2.txt
   ```
   Utdata:
   ```
   file1.txt
   file2.txt
   ```

4. Fjerne et spesifikt suffiks fra flere filer:
   ```sh
   basename -s .txt /path/to/file1.txt /path/to/file2.txt
   ```
   Utdata:
   ```
   file1
   file2
   ```

## Tips
- Bruk `basename` når du jobber med skript for å håndtere filnavn dynamisk.
- Kombiner `basename` med andre kommandoer som `find` for å effektivt navigere i filsystemet.
- Vær oppmerksom på at `basename` ikke endrer filene; det returnerer bare navnet.