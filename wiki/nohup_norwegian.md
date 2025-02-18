# [Norsk] Debian Almquist Shell (dash) nohup bruk: Kjører kommandoer uten å bli avbrutt

## Oversikt
`nohup` (no hang up) er et kommandoverktøy som lar deg kjøre prosesser i bakgrunnen, selv etter at du har logget ut av terminalen. Dette er spesielt nyttig for langvarige oppgaver som du ønsker å fortsette å kjøre uten avbrudd.

## Bruk
Grunnleggende syntaks for `nohup`-kommandoen er som følger:

```
nohup [alternativer] [argumenter]
```

## Vanlige alternativer
- `&` - Kjører kommandoen i bakgrunnen.
- `-h` - Viser hjelp for kommandoen.
- `-p` - Angir prosess-ID for en eksisterende prosess.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `nohup`:

1. Kjøre et skript i bakgrunnen:
   ```bash
   nohup ./mitt_skript.sh &
   ```

2. Kjøre en langvarig oppgave og sende utdata til en fil:
   ```bash
   nohup long_running_command > output.log &
   ```

3. Kjøre en Python-applikasjon i bakgrunnen:
   ```bash
   nohup python3 min_applikasjon.py &
   ```

4. Kjøre en oppgave og ignorere utdata:
   ```bash
   nohup my_command > /dev/null 2>&1 &
   ```

## Tips
- Bruk `&` for å kjøre kommandoen i bakgrunnen, slik at du kan fortsette å bruke terminalen.
- Sjekk `nohup.out`-filen for utdata hvis du ikke spesifiserer en utdatafil.
- Vær oppmerksom på at `nohup` kun hindrer at prosessen blir avbrutt ved utlogging; det kan fortsatt bli stoppet av systemet hvis ressursene er begrenset.