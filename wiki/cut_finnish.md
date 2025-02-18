# [Suomi] Debian Almquist Shell (dash) cut käyttö: Tekstirivien leikkaaminen

## Yleiskatsaus
`cut`-komento on työkalu, jota käytetään tekstirivien leikkaamiseen ja tietojen erottamiseen. Se voi poimia tiettyjä osia tiedostosta tai syötteestä, mikä tekee siitä hyödyllisen esimerkiksi tiedon käsittelyssä ja analysoinnissa.

## Käyttö
Perussyntaksi `cut`-komennolle on seuraava:

```bash
cut [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`: Määrittää, mitkä kentät poimitaan (esim. `-f1` poimii ensimmäisen kentän).
- `-d`: Määrittää kenttien erottimen (oletuksena on tabulaattori).
- `-c`: Poimii tietyt merkit (esim. `-c1-5` poimii merkit 1-5).
- `--complement`: Poimii kaikki kentät, paitsi määritellyt.
- `-s`: Ohittaa tyhjät rivit.

## Yleiset esimerkit
### Esimerkki 1: Kenttien poimiminen
Poimi ensimmäinen kenttä tiedostosta, jossa kentät on eroteltu pilkuilla:

```bash
cut -d',' -f1 tiedosto.txt
```

### Esimerkki 2: Merkkien poimiminen
Poimi merkit 1-10 tiedostosta:

```bash
cut -c1-10 tiedosto.txt
```

### Esimerkki 3: Useiden kenttien poimiminen
Poimi ensimmäinen ja kolmas kenttä tiedostosta:

```bash
cut -d',' -f1,3 tiedosto.txt
```

### Esimerkki 4: Kenttien täydentäminen
Poimi kaikki kentät, paitsi toinen:

```bash
cut -d',' -f --complement 2 tiedosto.txt
```

## Vinkit
- Käytä `-s`-vaihtoehtoa, jos haluat ohittaa tyhjät rivit tuloksista.
- Voit yhdistää `cut`-komennon muihin komentoihin, kuten `grep` tai `sort`, putkittamalla tuloksia.
- Testaa komento ensin pienellä tiedostolla varmistaaksesi, että se toimii odotetusti ennen kuin käytät sitä suuremmissa tiedostoissa.