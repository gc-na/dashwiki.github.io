# [Suomi] Debian Almquist Shell (dash) comm: vertaa kahta tiedostoa

## Yleiskatsaus
`comm`-komento on työkalu, jota käytetään kahden lajitellun tiedoston vertailuun. Se näyttää rivit, jotka ovat vain ensimmäisessä tiedostossa, vain toisessa tiedostossa ja rivit, jotka ovat molemmissa tiedostoissa.

## Käyttö
Perussyntaksi komennolle on seuraava:
```bash
comm [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-1`: Poistaa ensimmäisen tiedoston yksinomaan rivit tulosteesta.
- `-2`: Poistaa toisen tiedoston yksinomaan rivit tulosteesta.
- `-3`: Poistaa molempien tiedostojen yhteiset rivit tulosteesta.
- `-i`: Ignoroi suur- ja pienikirjaimisuuden vertailussa.

## Yleiset esimerkit
### Esimerkki 1: Perusvertailu
Vertaa kahta tiedostoa `file1.txt` ja `file2.txt`:
```bash
comm file1.txt file2.txt
```

### Esimerkki 2: Poista ensimmäisen tiedoston rivit
Näytä vain rivit, jotka ovat `file2.txt`:ssä:
```bash
comm -13 file1.txt file2.txt
```

### Esimerkki 3: Poista toisen tiedoston rivit
Näytä vain rivit, jotka ovat `file1.txt`:ssä:
```bash
comm -23 file1.txt file2.txt
```

### Esimerkki 4: Ignoroi suur- ja pienikirjaimisuus
Vertaa tiedostoja ilman huomioimatta kirjainkokoa:
```bash
comm -i file1.txt file2.txt
```

## Vinkit
- Varmista, että tiedostot ovat lajiteltuja ennen `comm`-komennon käyttöä, sillä se vaatii lajitellut syötteet.
- Voit yhdistää `comm`-komennon muihin komentoihin, kuten `sort`, lajitellaksesi tiedostot automaattisesti ennen vertailua:
  ```bash
  comm <(sort file1.txt) <(sort file2.txt)
  ```
- Käytä `-` merkkiä tiedostona, jos haluat lukea syötteen suoraan komentoriviltä.