# [Suomi] Debian Almquist Shell (dash) ls käyttö: tiedostojen ja kansioiden listaaminen

## Yleiskatsaus
`ls`-komento on käytössä Unix-tyyppisissä käyttöjärjestelmissä, kuten Debianissa, ja sen avulla voidaan listata hakemistossa olevat tiedostot ja kansiot. Tämä komento on yksi peruskomentoja, joita käytetään tiedostojärjestelmän tutkimiseen.

## Käyttö
Perussyntaksi `ls`-komennolle on seuraava:

```bash
ls [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Näyttää tiedostot pitkässä muodossa, mukaan lukien tiedoston oikeudet, omistaja, koko ja viimeisin muokkausaika.
- `-a`: Näyttää myös piilotetut tiedostot, joiden nimet alkavat pisteellä (`.`).
- `-h`: Näyttää tiedostojen koon ihmislukemassa muodossa (esim. Kt, Mt).
- `-R`: Listaa hakemistot ja niiden sisällön rekursiivisesti.

## Yleiset esimerkit
1. Peruslistaus nykyisessä hakemistossa:
   ```bash
   ls
   ```

2. Pitkä lista, joka näyttää tiedostojen tiedot:
   ```bash
   ls -l
   ```

3. Kaikkien tiedostojen, mukaan lukien piilotettujen, listaaminen:
   ```bash
   ls -a
   ```

4. Pitkä lista ihmislukemassa muodossa:
   ```bash
   ls -lh
   ```

5. Rekursiivinen listaus kaikista alihakemistoista:
   ```bash
   ls -R
   ```

## Vinkit
- Käytä `ls -lh` saadaksesi tiedostojen koon helposti luettavassa muodossa.
- Voit yhdistää useita vaihtoehtoja, esimerkiksi `ls -la` näyttää kaikki tiedostot pitkässä muodossa.
- Muista, että `ls` ei näytä tiedostoja, jotka ovat piilotettuja, ellei käytä `-a`-vaihtoehtoa.