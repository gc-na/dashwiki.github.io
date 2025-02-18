# [Suomi] Debian Almquist Shell (dash) lsof käyttö: tiedostojen ja prosessien tarkastelu

## Yleiskatsaus
`lsof` (list open files) on komento, jota käytetään näyttämään kaikki avoimet tiedostot ja niiden yhteydessä olevat prosessit. Tämä komento on erityisen hyödyllinen järjestelmänvalvojille, jotka haluavat seurata tiedostojen käyttöä ja prosessien toimintaa.

## Käyttö
Perussyntaksi `lsof`-komennolle on seuraava:

```bash
lsof [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-u [käyttäjä]`: Näyttää vain tietyn käyttäjän prosessit.
- `-p [prosessi]`: Näyttää vain tietyn prosessin avoimet tiedostot.
- `-i`: Näyttää verkko- ja internet-yhteydet.
- `+D [hakemisto]`: Näyttää kaikki tiedostot, jotka sijaitsevat tietyssä hakemistossa.
- `-t`: Tulostaa vain prosessien tunnukset (PID).

## Yleiset esimerkit
1. **Kaikkien avoimien tiedostojen näyttäminen:**
   ```bash
   lsof
   ```

2. **Tietyn käyttäjän prosessien näyttäminen:**
   ```bash
   lsof -u käyttäjänimi
   ```

3. **Tietyn prosessin avoimien tiedostojen näyttäminen:**
   ```bash
   lsof -p 1234
   ```

4. **Verkkoyhteyksien tarkastelu:**
   ```bash
   lsof -i
   ```

5. **Tiedostojen näyttäminen tietyssä hakemistossa:**
   ```bash
   lsof +D /polku/hakemistoon
   ```

## Vinkit
- Käytä `lsof`-komentoa yhdessä `grep`-komennon kanssa suodattaaksesi tuloksia tarkemmin.
- Muista, että `lsof`-komennon suorittaminen voi vaatia järjestelmänvalvojan oikeuksia, joten käytä tarvittaessa `sudo`-komentoa.
- Hyödynnä `-t`-vaihtoehtoa, jos haluat vain prosessitunnukset jatkokäsittelyä varten, kuten tappamista tai muita komentoja varten.