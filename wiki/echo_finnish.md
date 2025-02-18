# [Suomi] Debian Almquist Shell (dash) echo käyttö: Tulostaa merkkijonoja

## Yleiskatsaus
`echo`-komento on yksinkertainen työkalu, joka tulostaa merkkijonoja tai muuttujien arvoja komentoriville. Se on hyödyllinen esimerkiksi skriptien kirjoittamisessa, kun halutaan näyttää käyttäjälle tietoa tai tulostaa muuttujien sisältöä.

## Käyttö
Perussyntaksi `echo`-komennolle on seuraava:

```sh
echo [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n`: Älä tulosta rivinvaihtoa lopussa.
- `-e`: Ota käyttöön erityiset merkit, kuten `\n` (rivinvaihto) ja `\t` (tabulaattori).
- `-E`: Estä erityisten merkkien käyttö (oletusarvo).

## Yleiset esimerkit
Tulostetaan yksinkertainen merkkijono:

```sh
echo "Hei maailma!"
```

Tulostetaan merkkijono ilman rivinvaihtoa:

```sh
echo -n "Tämä on ilman rivinvaihtoa."
```

Tulostetaan merkkijono, jossa käytetään erityisiä merkkejä:

```sh
echo -e "Rivi 1\nRivi 2"
```

Tulostetaan muuttujan arvo:

```sh
nimi="Matti"
echo "Terve, $nimi!"
```

## Vinkit
- Käytä `-n`-vaihtoehtoa, kun haluat tulostaa useita merkkijonoja samalla rivillä.
- Muista käyttää lainausmerkkejä merkkijonojen ympärillä, erityisesti jos ne sisältävät välilyöntejä tai erityisiä merkkejä.
- Voit yhdistää useita merkkijonoja käyttämällä muuttujia ja `echo`-komentoa, mikä tekee skripteistäsi dynaamisempia.