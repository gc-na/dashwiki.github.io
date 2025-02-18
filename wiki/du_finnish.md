# [Suomi] Debian Almquist Shell (dash) du käyttö: Tiedostojen ja hakemistojen koon tarkastelu

## Yleiskatsaus
`du` (disk usage) on komento, jota käytetään tiedostojen ja hakemistojen koon tarkasteluun Unix- ja Linux-järjestelmissä. Se näyttää, kuinka paljon levytilaa tiedostot ja hakemistot vievät.

## Käyttö
Perussyntaksi `du`-komennolle on seuraava:

```bash
du [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`: Näyttää koot inhimillisessä muodossa (esim. KB, MB, GB).
- `-s`: Näyttää vain yhteenvedon hakemiston koosta, ei alihakemistoja.
- `-a`: Näyttää tiedostojen ja hakemistojen koon erikseen.
- `-c`: Laskee yhteen kaikkien näyttöön tulevien hakemistojen ja tiedostojen koot.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `du`-komennon käytöstä:

1. Näytä nykyisen hakemiston tiedostojen ja alihakemistojen koot:
   ```bash
   du
   ```

2. Näytä nykyisen hakemiston koot inhimillisessä muodossa:
   ```bash
   du -h
   ```

3. Näytä vain yhteenvedot kaikista alihakemistoista:
   ```bash
   du -s
   ```

4. Näytä kaikkien tiedostojen ja hakemistojen koot inhimillisessä muodossa:
   ```bash
   du -ah
   ```

5. Laske yhteen kaikkien hakemistojen koot ja näytä yhteenveto:
   ```bash
   du -c
   ```

## Vinkit
- Käytä `-h`-vaihtoehtoa aina, kun haluat helpommin luettavaa tietoa.
- Yhdistä `du`-komento muihin komentoihin, kuten `sort`, saadaksesi järjestetyn listan koosta.
- Varmista, että käytät `-s`-vaihtoehtoa suurissa hakemistoissa, jotta saat vain yhteenvedon, mikä voi nopeuttaa suorittamista.