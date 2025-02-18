# [Suomi] Debian Almquist Shell (dash) pidstat käyttö: prosessien tilastointi

## Yleiskatsaus
`pidstat` on komento, joka näyttää prosessien suorituskykytilastoja. Se voi seurata CPU:n käyttöä, muistinkäyttöä ja muita tärkeitä tietoja eri prosesseista järjestelmässä.

## Käyttö
Perussyntaksi komennolle on seuraava:
```
pidstat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`: Näyttää tulokset ihmislukuisessa muodossa.
- `-r`: Näyttää muistinkäyttötiedot.
- `-u`: Näyttää CPU:n käyttöasteen.
- `-p <PID>`: Seuraa tiettyä prosessia sen prosessitunnuksen (PID) perusteella.
- `-t`: Näyttää säikeiden tilastot.

## Yleiset esimerkit
Seuraavassa on muutamia käytännön esimerkkejä `pidstat`-komennon käytöstä:

1. **Seuraa kaikkien prosessien CPU:n käyttöä:**
   ```bash
   pidstat
   ```

2. **Seuraa tietyn prosessin (esim. PID 1234) CPU:n käyttöä:**
   ```bash
   pidstat -p 1234
   ```

3. **Näytä muistinkäyttötilastot kaikille prosesseille:**
   ```bash
   pidstat -r
   ```

4. **Seuraa prosessien tilastoja 5 sekunnin välein:**
   ```bash
   pidstat 5
   ```

5. **Näytä sekä CPU- että muistinkäyttötilastot:**
   ```bash
   pidstat -u -r
   ```

## Vinkit
- Käytä `pidstat`-komentoa yhdessä muiden järjestelmänvalvontatyökalujen kanssa, kuten `top` tai `htop`, saadaksesi kattavamman kuvan järjestelmän suorituskyvystä.
- Voit ohjata `pidstat`-komennon tulosteet tiedostoon analysointia varten lisäämällä `> tulostetiedosto.txt` komennon loppuun.
- Hyödynnä aikarajoja, kuten `pidstat 1`, saadaksesi reaaliaikaisia tietoja prosessien suorituskyvystä.