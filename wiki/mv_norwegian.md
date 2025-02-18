# [Norsk] Debian Almquist Shell (dash) mv Bruk: Flytt eller omdøp filer og kataloger

## Oversikt
`mv`-kommandoen brukes til å flytte eller omdøpe filer og kataloger i Linux. Den er en enkel, men kraftig kommando som gjør det mulig å organisere filene dine effektivt.

## Bruk
Grunnleggende syntaks for `mv`-kommandoen er som følger:

```bash
mv [alternativer] [kilder] [mål]
```

## Vanlige alternativer
- `-i`: Spør før overskriving av eksisterende filer.
- `-u`: Flytt bare hvis kilden er nyere enn målet eller hvis målet ikke eksisterer.
- `-v`: Vis detaljer om hva som blir gjort (verbose).
- `-n`: Ikke overskriv eksisterende filer.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `mv` kan brukes:

1. **Flytte en fil til en annen katalog:**
   ```bash
   mv fil.txt /sti/til/mål/katalog/
   ```

2. **Omdøpe en fil:**
   ```bash
   mv gammelt_navn.txt nytt_navn.txt
   ```

3. **Flytte flere filer til en katalog:**
   ```bash
   mv fil1.txt fil2.txt /sti/til/mål/katalog/
   ```

4. **Bruke alternativet -i for å unngå overskriving:**
   ```bash
   mv -i fil.txt /sti/til/mål/katalog/
   ```

5. **Flytte en katalog:**
   ```bash
   mv /sti/til/gammel_katalog /sti/til/ny_katalog/
   ```

## Tips
- Bruk `-v` for å se hva som skjer når du flytter filer, spesielt når du jobber med mange filer.
- Vær forsiktig med `mv`-kommandoen, da den kan overskrive filer uten advarsel hvis du ikke bruker alternativet `-i`.
- Når du omdøper filer, sørg for at det nye navnet ikke allerede eksisterer i målområdet, med mindre du ønsker å overskrive det.