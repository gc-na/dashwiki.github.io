# [Suomi] Debian Almquist Shell (dash) tee käyttö: Tietojen ohjaaminen useisiin kohteisiin

## Yleiskatsaus
`tee`-komento on työkalu, joka lukee standardisyötteen ja kirjoittaa sen sekä standardilähtöön että yhteen tai useampaan tiedostoon. Tämä mahdollistaa tietojen tallentamisen samanaikaisesti näyttöön ja tiedostoon.

## Käyttö
Perussyntaksi `tee`-komennolle on seuraava:

```bash
tee [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`, `--append`: Lisää tiedot tiedoston loppuun sen sijaan, että ylikirjoittaisi sen.
- `-i`, `--ignore-interrupts`: Ohittaa keskeytyssignaalit.

## Yleiset esimerkit
1. **Perus käyttö**: Kirjoita komennon tulos tiedostoon ja näytä se myös näytöllä.
   ```bash
   echo "Terve maailma" | tee tiedosto.txt
   ```

2. **Lisääminen tiedostoon**: Lisää uusi rivi olemassa olevaan tiedostoon.
   ```bash
   echo "Uusi rivi" | tee -a tiedosto.txt
   ```

3. **Useiden tiedostojen kirjoittaminen**: Kirjoita sama tulos useisiin tiedostoihin.
   ```bash
   echo "Tiedot" | tee tiedosto1.txt tiedosto2.txt
   ```

4. **Käyttö yhdessä komennon kanssa**: Käytä `tee`-komentoa osana putkistoa.
   ```bash
   ls -l | tee tiedostot.txt | grep "hakemisto"
   ```

## Vinkit
- Käytä `-a`-vaihtoehtoa, kun haluat lisätä tietoja olemassa olevaan tiedostoon sen sijaan, että ylikirjoittaisit sen.
- Hyödynnä `tee`-komentoa putkistojen yhteydessä, jotta voit tarkistaa komennon tuloksen ennen sen tallentamista.
- Muista, että `tee` voi olla hyödyllinen skripteissä, joissa haluat tallentaa lokitietoja samalla kun suoritat komentoja.