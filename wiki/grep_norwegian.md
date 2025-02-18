# [Norsk] Debian Almquist Shell (dash) grep Bruk: Søk etter mønstre i tekst

## Oversikt
`grep` er et kraftig verktøy i Unix-lignende operativsystemer som brukes til å søke etter spesifikke mønstre i tekstfiler. Det står for "Global Regular Expression Print" og lar brukeren filtrere ut linjer som inneholder et bestemt mønster.

## Bruk
Den grunnleggende syntaksen for `grep` er som følger:

```bash
grep [alternativer] [mønster] [fil]
```

## Vanlige alternativer
- `-i`: Ignorerer store og små bokstaver (case insensitive).
- `-v`: Viser linjer som ikke matcher mønsteret.
- `-r`: Søker rekursivt i kataloger.
- `-n`: Viser linjenummeret til hver match.
- `-l`: Viser bare filnavnene som inneholder matchen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `grep` kan brukes:

1. Søke etter et spesifikt ord i en fil:
   ```bash
   grep "ord" fil.txt
   ```

2. Søke etter et ord uten å ta hensyn til store og små bokstaver:
   ```bash
   grep -i "ord" fil.txt
   ```

3. Vise linjenumrene til linjene som inneholder et bestemt mønster:
   ```bash
   grep -n "ord" fil.txt
   ```

4. Søke rekursivt i alle filer i en katalog:
   ```bash
   grep -r "ord" /sti/til/katalog
   ```

5. Vise linjer som ikke inneholder et bestemt mønster:
   ```bash
   grep -v "ord" fil.txt
   ```

## Tips
- Bruk `grep` sammen med andre kommandoer ved å bruke pipe (`|`) for å filtrere ut resultater. For eksempel:
  ```bash
  ls -l | grep "filnavn"
  ```
- For å søke etter flere mønstre, kan du bruke `-e` alternativet:
  ```bash
  grep -e "mønster1" -e "mønster2" fil.txt
  ```
- Lagre ofte brukte grep-kommandoer i et skript for å spare tid.