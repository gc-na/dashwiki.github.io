# [Suomi] Debian Almquist Shell (dash) true käyttö: aina onnistuva komento

## Yleiskatsaus
`true` on yksinkertainen komento, joka palauttaa aina onnistuneen (0) tilakoodin. Sitä käytetään usein skripteissä ja komentoissa, joissa tarvitaan onnistumisen vahvistamista ilman varsinaista toimintoa.

## Käyttö
Perussyntaksi komennolle on seuraava:
```sh
true [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- Ei erityisiä vaihtoehtoja, koska `true` ei vaadi lisäparametreja toimiakseen.

## Yleiset esimerkit
### Esimerkki 1: Perus käyttö
```sh
true
```
Tämä komento suoritetaan ja palauttaa onnistuneen tilakoodin.

### Esimerkki 2: Käyttö if-lauseessa
```sh
if true; then
    echo "Tämä tulostuu aina."
fi
```
Tässä `if`-lause tarkistaa `true`-komennon tilakoodin ja suorittaa tulostuksen, koska `true` palauttaa aina 0.

### Esimerkki 3: Komentojen yhdistäminen
```sh
true && echo "Ensimmäinen komento onnistui."
```
Tässä komento `echo` suoritetaan, koska edellinen komento `true` onnistui.

## Vinkit
- Käytä `true`-komentoa skripteissä, joissa haluat varmistaa, että komento ei aiheuta virhetilaa.
- `true` on hyödyllinen myös paikoissa, joissa tarvitaan komento, mutta ei haluta tehdä mitään varsinaista toimintoa.
- Voit käyttää `true`-komentoa testataksesi skriptin logiikkaa ilman, että se vaikuttaa muihin komentoihin.