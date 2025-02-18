# [Suomi] Debian Almquist Shell (dash) cd käyttö: Siirtyminen hakemistoon

## Yleiskatsaus
`cd`-komento (change directory) on käytettävä komento, jonka avulla voit siirtyä eri hakemistoihin komentorivillä. Tämä on tärkeä osa tiedostojärjestelmän navigointia, ja sen avulla voit helposti siirtyä haluamaasi sijaintiin.

## Käyttö
Perussyntaksi `cd`-komennolle on seuraava:

```sh
cd [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-`: Siirtyy edelliseen hakemistoon.
- `..`: Siirtyy ylöspäin yhden hakemiston.
- `~`: Siirtyy käyttäjän kotihakemistoon.

## Yleiset esimerkit
Siirry hakemistoon nimeltä "asiakirjat":

```sh
cd asiakirjat
```

Siirry ylöspäin yhden hakemiston:

```sh
cd ..
```

Siirry käyttäjän kotihakemistoon:

```sh
cd ~
```

Siirry edelliseen hakemistoon:

```sh
cd -
```

## Vinkit
- Käytä `cd`-komentoa yhdessä `ls`-komennon kanssa tarkistaaksesi nykyisen hakemiston sisällön.
- Voit käyttää tab-näppäintä hakemistojen automaattiseen täydentämiseen, mikä nopeuttaa navigointia.
- Muista, että hakemistopolut ovat tapausherkkiä, joten varmista, että kirjoitat hakemistojen nimet oikein.