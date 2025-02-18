# [Suomi] Debian Almquist Shell (dash) find käyttö: tiedostojen etsiminen

## Overview
`find`-komento on tehokas työkalu, jota käytetään tiedostojen etsimiseen ja hakemiseen tiedostojärjestelmästä. Sen avulla voit etsiä tiedostoja ja hakemistoja eri kriteerien, kuten nimen, koon tai muokkausajan perusteella.

## Usage
Perussyntaksi `find`-komennolle on seuraava:

```bash
find [options] [arguments]
```

## Common Options
- `-name <nimi>`: Etsi tiedostoja, joiden nimi vastaa annettua nimeä.
- `-type <tyyppi>`: Etsi tietyn tyyppisiä tiedostoja (esim. `f` tiedostoille, `d` hakemistoille).
- `-size <koko>`: Etsi tiedostoja, jotka ovat tietyn kokoisia.
- `-mtime <päivämäärä>`: Etsi tiedostoja, jotka on muokattu tietyn määrän päiviä sitten.
- `-exec <komento> {} \;`: Suorita komento jokaiselle löydetylle tiedostolle.

## Common Examples
Eri käytännön esimerkkejä `find`-komennosta:

1. Etsi kaikki `.txt`-tiedostot nykyisestä hakemistosta ja sen alihakemistoista:
   ```bash
   find . -name "*.txt"
   ```

2. Etsi kaikki hakemistot:
   ```bash
   find . -type d
   ```

3. Etsi tiedostot, jotka ovat suurempia kuin 1 megatavu:
   ```bash
   find . -size +1M
   ```

4. Etsi tiedostot, jotka on muokattu viimeisen 7 päivän aikana:
   ```bash
   find . -mtime -7
   ```

5. Poista kaikki `.tmp`-tiedostot:
   ```bash
   find . -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Käytä `-print`-valintoa, jos haluat varmistaa, että löydetyt tiedostot tulostuvat näytölle.
- Ole varovainen `-exec`-valinnan kanssa, erityisesti poistettaessa tiedostoja, varmista aina, että komento on oikea.
- Voit yhdistää useita ehtoja käyttämällä `-and` ja `-or` -operaattoreita.