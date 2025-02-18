# [Norsk] Debian Almquist Shell (dash) wc Bruk: Telle linjer, ord og tegn i filer

## Oversikt
`wc` (word count) er et nyttig kommandoverktøy som brukes til å telle linjer, ord og tegn i tekstfiler. Det gir en rask måte å få en oversikt over innholdet i filer og kan være nyttig i mange skripting- og programmeringsoppgaver.

## Bruk
Den grunnleggende syntaksen for `wc`-kommandoen er:

```bash
wc [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l`: Teller antall linjer i filen.
- `-w`: Teller antall ord i filen.
- `-c`: Teller antall tegn i filen.
- `-m`: Teller antall tegn (inkludert multibyte-tegn).
- `-L`: Viser lengden på den lengste linjen i filen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `wc` kan brukes:

1. **Telle linjer i en fil:**
   ```bash
   wc -l filnavn.txt
   ```

2. **Telle ord i en fil:**
   ```bash
   wc -w filnavn.txt
   ```

3. **Telle tegn i en fil:**
   ```bash
   wc -c filnavn.txt
   ```

4. **Telle linjer, ord og tegn samtidig:**
   ```bash
   wc filnavn.txt
   ```

5. **Bruke med flere filer:**
   ```bash
   wc fil1.txt fil2.txt
   ```

## Tips
- Du kan kombinere alternativer for å få mer spesifik informasjon. For eksempel, `wc -l -w filnavn.txt` vil gi deg både linje- og ordtellingen.
- Hvis du ønsker å bruke `wc` med utdata fra en annen kommando, kan du bruke en pipe. For eksempel:
  ```bash
  cat filnavn.txt | wc -l
  ```
- Vær oppmerksom på at `wc` også kan brukes med standard input, så du kan skrive tekst direkte i terminalen og deretter bruke Ctrl+D for å avslutte og få tellingen.