# [Suomi] Debian Almquist Shell (dash) trap käyttö: Käynnistää komentoja signaalien vastaanottamiseksi

## Yleiskatsaus
`trap`-komento on työkalu, jota käytetään signaalien käsittelemiseen shell-skripteissä. Se mahdollistaa tiettyjen komentojen suorittamisen, kun skripti vastaanottaa tiettyjä signaaleja, kuten keskeytyksiä tai poistumiskäskyjä. Tämä on hyödyllistä esimerkiksi siivouskomentojen suorittamiseksi ennen skriptin lopettamista.

## Käyttö
Perussyntaksi `trap`-komennolle on seuraava:

```sh
trap [options] [arguments]
```

## Yleiset vaihtoehdot
- `SIGINT`: Keskeytyssignaali (Ctrl+C).
- `SIGTERM`: Poistumissignaali.
- `EXIT`: Suoritetaan, kun skripti lopettaa.
- `ERR`: Suoritetaan, jos komento epäonnistuu.

## Yleiset esimerkit

### Esimerkki 1: Siivous ennen poistumista
```sh
trap 'echo "Skripti suljetaan"; rm -f /tmp/tempfile' EXIT
```
Tässä esimerkissä skripti tulostaa viestin ja poistaa väliaikaisen tiedoston, kun se suljetaan.

### Esimerkki 2: Keskeytyksen käsittely
```sh
trap 'echo "Keskeytyssignaali vastaanotettu!"' SIGINT
```
Tämä komento tulostaa viestin, kun käyttäjä painaa Ctrl+C.

### Esimerkki 3: Virheiden käsittely
```sh
trap 'echo "Virhe tapahtui!"' ERR
```
Tässä esimerkissä viesti tulostuu, jos jokin komento epäonnistuu skriptissä.

## Vinkit
- Käytä `trap`-komentoa aina, kun haluat varmistaa, että resurssit vapautetaan oikein skriptin lopussa.
- Muista testata skriptiäsi eri signaalien kanssa varmistaaksesi, että kaikki toimii odotetusti.
- Voit määrittää useita `trap`-komentoja eri signaaleille, mutta varmista, että ne eivät aiheuta ristiriitoja.