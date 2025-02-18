# [Suomi] Debian Almquist Shell (dash) printenv käyttö: Tulostaa ympäristömuuttujat

## Yleiskatsaus
`printenv`-komento tulostaa ympäristömuuttujat, jotka ovat käytettävissä nykyisessä komentotulkin istunnossa. Tämä komento on hyödyllinen, kun halutaan tarkistaa, mitkä muuttujat ovat asetettuina ja mitä arvoja niillä on.

## Käyttö
Perussyntaksi `printenv`-komennolle on seuraava:

```bash
printenv [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-0`, `--null`: Tulostaa ympäristömuuttujat null-terminoinnilla.
- `VARIABELLI`: Voit antaa muuttujan nimen tulostaaksesi vain sen arvon.

## Yleiset esimerkit
Tulostetaan kaikki ympäristömuuttujat:

```bash
printenv
```

Tulostetaan tietyn ympäristömuuttujan, esimerkiksi `HOME`, arvo:

```bash
printenv HOME
```

Tulostetaan ympäristömuuttujat null-terminoinnilla:

```bash
printenv -0
```

## Vinkit
- Käytä `printenv`-komentoa yhdessä putkien kanssa, kuten `grep`, suodattaaksesi tiettyjä muuttujia. Esimerkiksi:

```bash
printenv | grep PATH
```

- Muista, että `printenv` ei näytä muuttujia, jotka on asetettu vain nykyisessä skriptissä, ellei niitä ole myös ympäristömuuttujina.