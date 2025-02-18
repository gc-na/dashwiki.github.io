# [Suomi] Debian Almquist Shell (dash) exit käyttö: Poistu komentoriviltä

## Yleiskatsaus
`exit`-komento sulkee nykyisen komentorivisession. Se on erityisen hyödyllinen, kun haluat lopettaa skriptin tai poistua interaktiivisesta shell-istunnosta.

## Käyttö
Perussyntaksi `exit`-komennolle on seuraava:

```sh
exit [options] [arguments]
```

## Yleiset vaihtoehdot
- `n`: Voit määrittää poistumiskoodin, joka on kokonaisluku. Oletusarvoisesti se on 0, mikä tarkoittaa, että poistuminen tapahtui onnistuneesti.

## Yleiset esimerkit

### Esimerkki 1: Poistu ilman koodia
Voit yksinkertaisesti käyttää `exit`-komentoa poistuaksesi shellistä:

```sh
exit
```

### Esimerkki 2: Poistu tietyllä koodilla
Jos haluat poistaa shellin ja ilmoittaa, että tapahtui virhe, voit käyttää seuraavaa komentoa:

```sh
exit 1
```

### Esimerkki 3: Poistu skriptistä
Voit käyttää `exit`-komentoa skriptissä lopettaaksesi sen suorittamisen:

```sh
#!/bin/dash
echo "Skripti käynnistyy..."
exit 0
```

## Vinkit
- Käytä `exit`-komentoa aina, kun haluat varmistaa, että skripti tai istunto päättyy oikein.
- Muista, että poistumiskoodi voi olla hyödyllinen virheiden käsittelyssä, joten määritä se tarvittaessa.
- Voit tarkistaa edellisen komennon poistumiskoodin käyttämällä `$?`-muuttujaa.