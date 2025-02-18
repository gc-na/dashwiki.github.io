# [Suomi] Debian Almquist Shell (dash) dstat käyttö: järjestelmän resurssien seuranta

## Yleiskatsaus
`dstat` on tehokas komento, joka yhdistää useita järjestelmän resurssien seurannan työkaluja yhdeksi käteväksi työkaluksi. Se mahdollistaa reaaliaikaisen seurannan eri resurssien, kuten prosessorin, muistin, levyjen ja verkon, käytöstä.

## Käyttö
Perussyntaksi dstat-komennolle on seuraava:

```bash
dstat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Näyttää prosessorin käytön.
- `-d`: Näyttää levyn käytön.
- `-n`: Näyttää verkkoliikenteen.
- `-m`: Näyttää muistin käytön.
- `--help`: Näyttää ohjeet ja käytettävissä olevat vaihtoehdot.

## Yleiset esimerkit
Seuraavassa on muutamia käytännön esimerkkejä dstat-komennon käytöstä:

1. **Perusresurssien seuranta:**
   ```bash
   dstat
   ```

2. **Prosessorin ja muistin käytön seuraaminen:**
   ```bash
   dstat -c -m
   ```

3. **Levy- ja verkkoliikenteen seuraaminen:**
   ```bash
   dstat -d -n
   ```

4. **Kaikkien resurssien seuraaminen reaaliaikaisesti:**
   ```bash
   dstat -cdnm
   ```

5. **Tietojen tallentaminen tiedostoon:**
   ```bash
   dstat -cdmn --output dstat_output.csv
   ```

## Vinkit
- Käytä `dstat`-komentoa yhdessä muiden komentojen, kuten `grep` tai `less`, kanssa, jotta voit suodattaa tai tarkastella tietoja helpommin.
- Voit yhdistää useita vaihtoehtoja saadaksesi tarkempaa tietoa järjestelmän tilasta.
- Muista tarkistaa dstatin dokumentaatio lisäasetusten ja vaihtoehtojen löytämiseksi, jotka voivat olla hyödyllisiä erityistarpeissasi.