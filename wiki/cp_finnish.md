# [Suomi] Debian Almquist Shell (dash) cp käyttö: Tiedostojen kopioiminen

## Yleiskatsaus
`cp`-komento on käytössä tiedostojen ja hakemistojen kopioimiseen Unix-tyyppisissä käyttöjärjestelmissä, kuten Debianissa. Sen avulla voit luoda kopioita tiedostoista ja siirtää niitä eri sijainteihin.

## Käyttö
Perussyntaksi `cp`-komennolle on seuraava:

```bash
cp [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-r`: Kopioi hakemiston ja sen sisällön rekursiivisesti.
- `-i`: Kysyy vahvistusta ennen olemassa olevan tiedoston ylikirjoittamista.
- `-u`: Kopioi vain, jos lähdetiedosto on uudempi kuin kohdetiedosto tai jos kohdetiedostoa ei ole.
- `-v`: Näyttää kopioitavat tiedostot komentorivillä.

## Yleiset esimerkit
Käytetään `cp`-komentoa eri tilanteissa:

1. Yksittäisen tiedoston kopioiminen:
   ```bash
   cp tiedosto.txt kopio_tiedosto.txt
   ```

2. Hakemiston kopioiminen rekursiivisesti:
   ```bash
   cp -r hakemisto/ kopio_hakemisto/
   ```

3. Tiedoston kopioiminen vahvistuksen kanssa:
   ```bash
   cp -i tiedosto.txt kohde_tiedosto.txt
   ```

4. Vain uudemman tiedoston kopioiminen:
   ```bash
   cp -u tiedosto.txt kohde_tiedosto.txt
   ```

5. Kopioiminen näkyvällä tulostuksella:
   ```bash
   cp -v tiedosto.txt kohde_tiedosto.txt
   ```

## Vinkit
- Käytä `-i`-vaihtoehtoa, kun olet epävarma siitä, että haluat ylikirjoittaa olemassa olevan tiedoston.
- Muista käyttää `-r`-vaihtoehtoa, kun kopioit hakemistoja, jotta kaikki alihakemistot ja tiedostot kopioituvat.
- Voit yhdistää useita vaihtoehtoja, esimerkiksi `cp -riv tiedosto.txt kohde_tiedosto.txt` kopioi tiedoston ja näyttää prosessin samalla.
- Tarkista aina kohdepolku ennen kopioimista, jotta tiedostot menevät oikeaan paikkaan.