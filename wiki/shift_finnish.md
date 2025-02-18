# [Suomi] Debian Almquist Shell (dash) shift käyttö: Siirtää argumentteja

## Yleiskatsaus
`shift`-komento käytetään argumenttien siirtämiseen komentorivillä. Se poistaa ensimmäisen argumentin ja siirtää jäljelle jääneet argumentit vasemmalle, jolloin uusi ensimmäinen argumentti tulee käyttöön.

## Käyttö
Perussyntaksi `shift`-komennolle on seuraava:

```bash
shift [n]
```

Missä `n` on valinnainen argumentti, joka määrittää, kuinka monta argumenttia siirretään.

## Yleiset vaihtoehdot
- `n`: Määrittää, kuinka monta argumenttia siirretään. Oletusarvo on 1, mikä tarkoittaa, että vain ensimmäinen argumentti poistetaan.

## Yleiset esimerkit

### Esimerkki 1: Perus käyttö
```bash
#!/bin/dash
set -- arg1 arg2 arg3
echo "Ennen shift: $1"  # Tulostaa "arg1"
shift
echo "Shiftin jälkeen: $1"  # Tulostaa "arg2"
```

### Esimerkki 2: Siirrä useita argumentteja
```bash
#!/bin/dash
set -- arg1 arg2 arg3 arg4
echo "Ennen shift: $1"  # Tulostaa "arg1"
shift 2
echo "Shiftin jälkeen: $1"  # Tulostaa "arg3"
```

### Esimerkki 3: Argumenttien käsittely silmukassa
```bash
#!/bin/dash
set -- arg1 arg2 arg3 arg4
while [ "$#" -gt 0 ]; do
    echo "Käsitellään: $1"
    shift
done
```

## Vinkit
- Käytä `shift`-komentoa yhdessä silmukoiden kanssa, kun haluat käsitellä useita argumentteja yksi kerrallaan.
- Muista tarkistaa argumenttien määrä ennen `shift`-komennon käyttöä, jotta vältät virheitä, kun yrität siirtää enemmän argumentteja kuin on saatavilla.
- `shift`-komennon käyttö voi helpottaa skriptien lukemista ja ylläpitoa, kun argumentteja käsitellään järjestelmällisesti.