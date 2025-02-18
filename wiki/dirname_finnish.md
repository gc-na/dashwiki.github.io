# [Suomi] Debian Almquist Shell (dash) dirname käyttö: [hakee tiedostopolkujen hakemistoja]

## Yleiskatsaus
`dirname`-komento on työkalu, joka palauttaa tiedostopolun hakemiston nimen. Se on hyödyllinen, kun haluat eristää tiedoston nimen sen polusta ja saada vain sen hakemiston.

## Käyttö
Perussyntaksi `dirname`-komennolle on seuraava:
```
dirname [options] [arguments]
```

## Yleiset vaihtoehdot
- `-z`: Tuottaa tulosteen nollan päättävänä merkkijonona.
- `--help`: Näyttää apuviestin ja käytön.
- `--version`: Näyttää ohjelman version.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `dirname`-komennon käytöstä:

1. Hanki hakemisto tiedostopolusta:
   ```sh
   dirname /home/kayttaja/tiedostot/kuva.png
   ```
   Tulostaa:
   ```
   /home/kayttaja/tiedostot
   ```

2. Hanki hakemisto tiedostopolusta ilman tiedostopäätettä:
   ```sh
   dirname /var/log/syslog
   ```
   Tulostaa:
   ```
   /var/log
   ```

3. Käytä `dirname` yhdessä muiden komentojen kanssa:
   ```sh
   echo "Hakemisto: $(dirname /usr/local/bin/script.sh)"
   ```
   Tulostaa:
   ```
   Hakemisto: /usr/local/bin
   ```

## Vinkit
- Voit käyttää `dirname`-komentoa putkittamalla sen muiden komentojen kanssa, kuten `xargs`, jotta voit käsitellä useita tiedostoja kerralla.
- Muista, että `dirname` palauttaa vain hakemiston nimen, joten jos tarvitset tiedoston nimen, käytä `basename`-komentoa sen sijaan.
- Hyödynnä `dirname`-komentoa skripteissä, kun haluat automatisoida tiedostopolkujen käsittelyä.