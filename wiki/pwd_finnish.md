# [Suomi] Debian Almquist Shell (dash) pwd käyttö: Näyttää nykyisen työskentelyhakemiston

## Yleiskatsaus
`pwd` (print working directory) -komento näyttää nykyisen työskentelyhakemiston täydellisen polun. Tämä on erityisen hyödyllistä, kun haluat tietää, missä hakemistossa työskentelet, erityisesti monimutkaisissa hakemistorakenteissa.

## Käyttö
Perussyntaksi komennolle on seuraava:
```
pwd [options] [arguments]
```

## Yleiset vaihtoehdot
- `-L`: Näyttää symboliset linkit, mikä tarkoittaa, että se näyttää nykyisen hakemiston polun, joka voi sisältää linkkejä.
- `-P`: Näyttää fyysisen polun, joka ei sisällä symbolisia linkkejä.

## Yleiset esimerkit
1. Nykyisen hakemiston näyttäminen:
   ```sh
   pwd
   ```

2. Symbolisten linkkien näyttäminen:
   ```sh
   pwd -L
   ```

3. Fyysisen polun näyttäminen:
   ```sh
   pwd -P
   ```

## Vinkit
- Käytä `pwd`-komentoa säännöllisesti varmistaaksesi, että tiedät, missä hakemistossa olet, erityisesti kun navigoit syvälle hakemistopuihin.
- Yhdistä `pwd` muihin komentoihin, kuten `cd`, saadaksesi selkeämmän käsityksen hakemistosi rakenteesta.
- Muista, että `pwd` on hyödyllinen myös skripteissä, joissa tarvitset nykyisen hakemiston polkua jatkotoimille.