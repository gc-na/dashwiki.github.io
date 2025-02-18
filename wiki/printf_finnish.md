# [Suomi] Debian Almquist Shell (dash) printf käyttö: Muotoile ja tulosta tekstiä

## Yleiskatsaus
`printf`-komento on käytettävissä Debian Almquist Shellissä (dash) ja se mahdollistaa muotoillun tekstin tulostamisen konsoliin. Se on hyödyllinen työkalu, kun halutaan esittää tietoa tietyssä muodossa, kuten numeroiden, merkkijonojen tai muiden tietotyyppien kanssa.

## Käyttö
Perussyntaksi `printf`-komennolle on seuraava:

```sh
printf [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-v`: Määrittää muuttujan, johon tulostus tallennetaan.
- `-f`: Määrittää muotoilun, jota käytetään tulostuksessa.
- `--help`: Näyttää apua ja käytön ohjeita.

## Yleiset esimerkit
Esimerkki 1: Tulostaa yksinkertaisen merkkijonon.

```sh
printf "Hei, maailma!\n"
```

Esimerkki 2: Tulostaa muotoillun numeron.

```sh
printf "Luku: %.2f\n" 3.14159
```

Esimerkki 3: Tulostaa useita arvoja yhdellä komennolla.

```sh
printf "Nimi: %s, Ikä: %d\n" "Matti" 30
```

Esimerkki 4: Tallentaa tulostuksen muuttujaan.

```sh
printf -v tulos "Tulos: %.2f" 123.456
echo "$tulos"
```

## Vinkit
- Käytä `%s` merkkijonojen ja `%d` kokonaislukujen tulostamiseen.
- Muista lisätä `\n` rivinvaihdon vuoksi, jos haluat tulostaa useita rivejä.
- Testaa eri muotoiluvaihtoehtoja, kuten `%f` liukulukuja varten, saadaksesi haluamasi tulostusmuodon.