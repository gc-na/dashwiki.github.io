# [Norsk] Debian Almquist Shell (dash) strace bruksanvisning: Spore systemkall og signaler

## Oversikt
`strace` er et kraftig verktøy som brukes til å spore systemkall og signaler i et program. Det gir utviklere og systemadministratorer muligheten til å se hva som skjer bak kulissene når et program kjører, noe som er nyttig for feilsøking og ytelsesanalyse.

## Bruk
Grunnleggende syntaks for `strace`-kommandoen er som følger:

```bash
strace [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Oppsummerer statistikk om systemkallene som ble utført.
- `-e`: Filtrerer systemkallene som skal spores, for eksempel `-e trace=open` for kun å spore åpning av filer.
- `-o filnavn`: Skriver ut sporing til en spesifisert fil i stedet for standard utgang.
- `-p prosess_id`: Sporer en allerede kjørende prosess ved å spesifisere dens prosess-ID.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `strace`:

1. Spore et nytt program:
   ```bash
   strace ls
   ```

2. Spore et program og skrive ut til en fil:
   ```bash
   strace -o output.txt ls
   ```

3. Spore spesifikke systemkall:
   ```bash
   strace -e trace=open ls
   ```

4. Spore en kjørende prosess:
   ```bash
   strace -p 1234
   ```

5. Oppsummere statistikk om systemkall:
   ```bash
   strace -c ls
   ```

## Tips
- Bruk `-o` alternativet for å lagre utdataene til en fil, slik at du kan analysere dem senere.
- Kombiner `-e` alternativet med spesifikke systemkall for å fokusere på det som er relevant for feilsøkingen din.
- Vær oppmerksom på at `strace` kan påvirke ytelsen til programmet som spores, så det er best å bruke det i et testmiljø når det er mulig.