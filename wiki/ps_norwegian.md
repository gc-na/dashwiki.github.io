# [Norsk] Debian Almquist Shell (dash) ps Bruk: Vise prosesser

## Oversikt
`ps`-kommandoen brukes til å vise informasjon om aktive prosesser i systemet. Den gir en oversikt over prosessene som kjører, inkludert prosess-ID, tilstand, og ressursbruk.

## Bruk
Grunnleggende syntaks for `ps`-kommandoen er som følger:
```
ps [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e` eller `-A`: Viser alle prosesser.
- `-f`: Viser full formatinformasjon, inkludert foreldrenes prosess-ID.
- `-u [brukernavn]`: Viser prosesser for en spesifikk bruker.
- `-o [format]`: Angir formatet for utdataene, for eksempel `pid,comm`.
- `--sort [felt]`: Sorterer prosessene etter det angitte feltet, som `pid` eller `time`.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `ps`-kommandoen:

1. Vise alle prosesser:
   ```bash
   ps -e
   ```

2. Vise prosesser med full formatinformasjon:
   ```bash
   ps -f
   ```

3. Vise prosesser for en spesifikk bruker:
   ```bash
   ps -u username
   ```

4. Vise prosesser sortert etter prosess-ID:
   ```bash
   ps --sort pid
   ```

5. Vise spesifikke felter for prosessene:
   ```bash
   ps -o pid,comm
   ```

## Tips
- Bruk `man ps` for å få mer detaljert informasjon om tilgjengelige alternativer og bruken av `ps`.
- Kombiner `ps` med `grep` for å filtrere prosesser. For eksempel:
  ```bash
  ps -e | grep bash
  ```
- Husk at `ps` viser en snapshot av prosessene på tidspunktet kommandoen kjøres; for kontinuerlig overvåking kan `top` eller `htop` være mer passende.