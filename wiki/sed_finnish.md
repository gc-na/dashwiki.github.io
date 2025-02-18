# [Suomi] Debian Almquist Shell (dash) sed käyttö: Tekstinkäsittely ja muokkaus

## Yleiskatsaus
`sed` (stream editor) on tehokas komentorivityökalu, jota käytetään tekstin muokkaamiseen ja käsittelyyn. Se mahdollistaa tekstin etsimisen, korvaamisen ja muokkaamisen reaaliaikaisesti syötteestä, mikä tekee siitä hyödyllisen monissa skripti- ja automaatiohankkeissa.

## Käyttö
Perussyntaksi `sed`-komennolle on seuraava:

```bash
sed [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e`: Lisää komentoja, joita `sed` suorittaa.
- `-i`: Muokkaa tiedostoa paikallisesti (in-place).
- `-n`: Estää tulostamisen, ellei sitä erikseen pyydetä.
- `s/pattern/replacement/`: Etsii ja korvataan `pattern`-ilmaisu `replacement`-ilmaisulla.

## Yleiset esimerkit

### 1. Tekstin korvaaminen
Korvataan kaikki esiintymät sanasta "vanha" sanalla "uusi" tiedostossa `tiedosto.txt`.

```bash
sed 's/vanha/uusi/g' tiedosto.txt
```

### 2. Muokkaus paikallisesti tiedostossa
Korvataan "vanha" "uusi" suoraan tiedostossa `tiedosto.txt`.

```bash
sed -i 's/vanha/uusi/g' tiedosto.txt
```

### 3. Rivien tulostaminen
Tulostetaan vain rivit, jotka sisältävät sanan "esimerkki".

```bash
sed -n '/esimerkki/p' tiedosto.txt
```

### 4. Rivin poistaminen
Poistetaan rivit, jotka sisältävät sanan "poista".

```bash
sed '/poista/d' tiedosto.txt
```

## Vinkit
- Käytä `-n`-vaihtoehtoa yhdessä `p`-komennon kanssa, jos haluat tulostaa vain tietyt rivit.
- Varmista, että teet varmuuskopion tiedostosta ennen kuin käytät `-i`-vaihtoehtoa, jotta et menetä alkuperäistä tietoa.
- Hyödynnä säännöllisiä lausekkeita monimutkaisemmissa muokkauksissa, mutta varmista, että ymmärrät niiden syntaksin.