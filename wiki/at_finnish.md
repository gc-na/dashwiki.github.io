# [Suomi] Debian Almquist Shell (dash) at käyttö: Ajastaa komentoja tulevaisuudessa

## Yleiskatsaus
`at`-komento mahdollistaa komentojen ajastamisen suoritettavaksi tiettynä ajankohtana tulevaisuudessa. Tämä on hyödyllistä, kun haluat suorittaa tehtäviä automaattisesti ilman, että sinun tarvitsee olla kirjautuneena sisään.

## Käyttö
Perussyntaksi `at`-komennolle on seuraava:

```bash
at [options] [arguments]
```

## Yleiset vaihtoehdot
- `-f` : Määrittää tiedoston, jonka sisältö suoritetaan.
- `-m` : Lähettää sähköpostiviestin, kun komento on suoritettu.
- `-q` : Määrittää jonon, johon komento lisätään.
- `-l` : Listaa kaikki ajastetut komennot.
- `-d` : Poistaa ajastetun komennon.

## Yleiset esimerkit
### Esimerkki 1: Yksinkertainen komento ajastettuna
Ajastetaan `echo`-komento suoritettavaksi tänään klo 14:00.

```bash
echo "Hei maailma!" | at 14:00
```

### Esimerkki 2: Komento tiedostosta
Ajastetaan komento, joka suoritetaan tiedostosta.

```bash
at -f /polku/tiedostoon.sh 15:00
```

### Esimerkki 3: Ajastettujen komentojen listaaminen
Listataan kaikki ajastetut komennot.

```bash
at -l
```

### Esimerkki 4: Ajastetun komennon poistaminen
Poistetaan ajastettu komento, jonka ID on 5.

```bash
at -d 5
```

## Vinkit
- Varmista, että käytät oikeaa aikamuotoa, kuten `HH:MM` tai `now + 1 hour`.
- Käytä `-m`-optioita, jos haluat saada ilmoituksen, kun komento on suoritettu.
- Tarkista ajastetut komennot säännöllisesti, jotta et unohda niitä.