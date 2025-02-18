# [Norsk] Debian Almquist Shell (dash) time bruk: Mål tid for kommandoer

## Oversikt
`time`-kommandoen brukes til å måle hvor lang tid det tar å kjøre en spesifikk kommando. Den gir deg informasjon om både den totale tiden som er brukt, samt hvor mye av tiden som ble brukt i bruker- og systemmodus.

## Bruk
Grunnleggende syntaks for `time`-kommandoen er som følger:

```bash
time [alternativer] [argumenter]
```

## Vanlige alternativer
- `-p`: Bruker POSIX-format for utdata.
- `-o fil`: Skriver utdata til den angitte filen.
- `-v`: Gir en detaljert rapport om ressursbruk.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `time` kan brukes:

1. Mål tiden for å kjøre et skript:
   ```bash
   time ./mitt_skript.sh
   ```

2. Mål tiden for å komprimere en mappe:
   ```bash
   time tar -czf arkiv.tar.gz /sti/til/mappe
   ```

3. Lagre tidsrapporten i en fil:
   ```bash
   time -o tid.txt ./min_kommando
   ```

4. Få detaljert informasjon om ressursbruk:
   ```bash
   time -v ./min_tunge_oppgave
   ```

## Tips
- Bruk `-p` for å få et enklere og mer lesbart format, spesielt når du jobber med skript.
- Hvis du kjører flere kommandoer, kan du bruke `time` foran hver for å få individuelle tidsmålinger.
- Vær oppmerksom på at `time` kan ha forskjellig oppførsel avhengig av hvilken shell du bruker, så sjekk dokumentasjonen for din spesifikke shell hvis du opplever problemer.