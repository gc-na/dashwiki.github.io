# [Suomi] Debian Almquist Shell (dash) expr käyttö: laskentatehtävien suorittaminen

## Overview
`expr` on komentorivikäsky, jota käytetään yksinkertaisten laskentatehtävien suorittamiseen, kuten yhteenlaskuun, vähennykseen, kertolaskuun ja jakamiseen. Se voi myös käsitellä merkkijonoja ja vertailuja.

## Usage
Perussyntaksi `expr`-komennolle on seuraava:

```bash
expr [options] [arguments]
```

## Common Options
- `-e`: Käytä laajennettua syntaksia.
- `-s`: Poista tulosteen väliin jäävät tyhjät merkit.
- `-m`: Käytä monimutkaisempaa laskentaa (esim. merkkijonojen käsittely).

## Common Examples
### Yhteenlasku
Yhdistele kaksi lukua yhteen:

```bash
expr 5 + 3
```

### Vähennys
Vähennä toinen luku ensimmäisestä:

```bash
expr 10 - 4
```

### Kertolasku
Kerro kaksi lukua:

```bash
expr 6 \* 7
```

### Jakaminen
Jaa luku toisella:

```bash
expr 20 / 4
```

### Merkkijonojen pituus
Laske merkkijonon pituus:

```bash
expr length "Hello"
```

### Vertailu
Tarkista, onko kaksi lukua yhtä suuret:

```bash
expr 5 = 5
```

## Tips
- Muista käyttää kenoviivaa (`\`) kertolaskun yhteydessä, jotta se ei sekoitu shellin omiin operaatioihin.
- `expr` palauttaa arvon, joten voit tallentaa tuloksen muuttujaan:

```bash
result=$(expr 5 + 3)
echo $result
```

- Käytä `expr`-komentoa vain yksinkertaisiin laskentatehtäviin; monimutkaisemmissa laskentatehtävissä kannattaa harkita muita työkaluja, kuten `bc` tai `awk`.