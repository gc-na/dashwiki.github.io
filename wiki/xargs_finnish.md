# [Suomi] Debian Almquist Shell (dash) xargs käyttö: Komentojen yhdistäminen

## Yleiskatsaus
`xargs` on komentorivityökalu, joka lukee syötteen standardista ja muuntaa sen argumenteiksi toiselle komennolle. Tämä on erityisen hyödyllistä, kun käsitellään suuria määriä tiedostoja tai tietoja, jotka ylittävät komentorivin pituusrajoitukset.

## Käyttö
Perussyntaksi `xargs`-komennolle on seuraava:

```bash
xargs [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n N`: Määrittää, kuinka monta argumenttia `xargs` syöttää kerralla.
- `-d DELIMITER`: Määrittää erottimen, jota käytetään syötteen lukemiseen.
- `-p`: Kysyy käyttäjältä vahvistuksen ennen komennon suorittamista.
- `-0`: Lukee syötteen nollan (null) erottimilla, mikä on hyödyllistä tiedostoille, joissa on välilyöntejä.

## Yleiset esimerkit

### Esimerkki 1: Tiedostojen poistaminen
Poista kaikki `.tmp`-tiedostot nykyisestä hakemistosta:

```bash
find . -name "*.tmp" | xargs rm
```

### Esimerkki 2: Tiedostojen siirtäminen
Siirrä kaikki `.jpg`-tiedostot toiseen hakemistoon:

```bash
find . -name "*.jpg" | xargs -I {} mv {} /polku/uuteen/hakemistoon/
```

### Esimerkki 3: Komennon suorittaminen useilla argumenteilla
Suorita `echo` komento jokaiselle syötteelle:

```bash
echo -e "tiedosto1\ntiedosto2\ntiedosto3" | xargs -n 1 echo
```

## Vinkit
- Käytä `-0`-vaihtoehtoa, kun käsittelet tiedostoja, joissa on välilyöntejä tai erikoismerkkejä.
- Varmista, että komento, jota käytät `xargs`-kanssa, voi käsitellä useita argumentteja kerralla, jotta vältät virheitä.
- Testaa komento ensin `-p`-vaihtoehdolla, jotta voit varmistaa, että se toimii odotetusti ennen varsinaista suorittamista.