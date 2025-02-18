# [Suomi] Debian Almquist Shell (dash) test käyttö: testaa ehtoja

## Yleiskatsaus
`test`-komento on käytännöllinen työkalu, jota käytetään ehtojen arvioimiseen skripteissä ja komentorivillä. Se voi tarkistaa erilaisia asioita, kuten tiedostojen olemassaolon, vertailuja ja muita ehtoja, palauttaen arvon, joka kertoo, onko ehto tosi vai epätosi.

## Käyttö
Perussyntaksi `test`-komennolle on seuraava:

```sh
test [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e [tiedosto]`: Tarkistaa, onko tiedosto olemassa.
- `-f [tiedosto]`: Tarkistaa, onko tiedosto tavallinen tiedosto.
- `-d [hakemisto]`: Tarkistaa, onko hakemisto olemassa.
- `-z [merkkijono]`: Tarkistaa, onko merkkijono tyhjää.
- `-eq`, `-ne`, `-lt`, `-le`, `-gt`, `-ge`: Käytetään numeerisiin vertailuihin (esim. `-eq` tarkoittaa "yhtä suuri kuin").

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `test`-komennon käytöstä:

### Esimerkki 1: Tiedoston olemassaolon tarkistus
```sh
test -e /path/to/file && echo "Tiedosto löytyy."
```

### Esimerkki 2: Tarkista, onko tiedosto tavallinen tiedosto
```sh
test -f /path/to/file && echo "Tämä on tavallinen tiedosto."
```

### Esimerkki 3: Tarkista, onko hakemisto olemassa
```sh
test -d /path/to/directory && echo "Hakemisto löytyy."
```

### Esimerkki 4: Merkkijonon tyhjyyden tarkistus
```sh
my_string=""
test -z "$my_string" && echo "Merkkijono on tyhjää."
```

### Esimerkki 5: Numeraalinen vertailu
```sh
a=5
b=10
test $a -lt $b && echo "$a on pienempi kuin $b."
```

## Vinkit
- Käytä `test`-komentoa yhdessä `if`-lausuntojen kanssa, jotta voit suorittaa ehtoja ja komentoja dynaamisesti.
- Muista käyttää lainausmerkkejä merkkijonojen ympärillä, jotta vältät virheitä tyhjien tai erikoismerkkien kanssa.
- Voit käyttää `[` ja `]` -merkkejä `test`-komennon sijasta, mikä tekee syntaksista hieman selkeämmän, esimerkiksi: `[ -e /path/to/file ]`.