# [Norsk] Debian Almquist Shell (dash) nice bruken: Juster prosessprioritet

## Oversikt
`nice`-kommandoen brukes til å starte prosesser med en spesifisert prioritet. Den lar brukeren justere hvor mye CPU-tid en prosess kan bruke, noe som er nyttig for å unngå at en enkelt prosess tar opp for mye ressurser.

## Bruk
Den grunnleggende syntaksen for `nice`-kommandoen er:

```bash
nice [alternativer] [kommando] [argumenter]
```

## Vanlige alternativer
- `-n, --adjustment`: Angi justeringsverdien for prioritet. Standardverdi er 10.
- `-h, --help`: Vis hjelpetekst for `nice`.
- `--version`: Vis versjonsinformasjon for `nice`.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `nice`:

1. Kjøre en prosess med lavere prioritet:
   ```bash
   nice -n 10 ./mitt_program
   ```

2. Kjøre en prosess med høyere prioritet:
   ```bash
   nice -n -5 ./kritisk_program
   ```

3. Sjekke den nåværende prioriteten til en prosess:
   ```bash
   ps -o pid,ni,comm
   ```

4. Starte en bakgrunnsprosess med lavere prioritet:
   ```bash
   nice -n 15 ./bakgrunnsoppgave &
   ```

## Tips
- Vær forsiktig med å bruke negative justeringsverdier, da dette kan påvirke systemets responsivitet.
- Bruk `top` eller `htop` for å overvåke prosessprioriteter og ressursbruk i sanntid.
- Kombiner `nice` med `nohup` for å kjøre lange prosesser i bakgrunnen uten at de avsluttes når terminalen lukkes.