# [Suomi] Debian Almquist Shell (dash) gzip käyttö: Tiedostojen pakkaaminen

## Yleiskatsaus
`gzip` on komento, jota käytetään tiedostojen pakkaamiseen, mikä vähentää niiden kokoa ja säästää tallennustilaa. Se käyttää Gzip-pakkausalgoritmia, joka on erityisen tehokas tekstimuotoisten tiedostojen kanssa.

## Käyttö
Perussyntaksi komennolle on seuraava:
```
gzip [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`, `--decompress`: Purkaa pakatut tiedostot.
- `-k`, `--keep`: Säilyttää alkuperäisen tiedoston pakkaamisen jälkeen.
- `-v`, `--verbose`: Näyttää yksityiskohtaisempaa tietoa pakkausprosessista.
- `-f`, `--force`: Pakkaa tiedoston, vaikka se olisi jo pakattu tai jos tiedosto on kirjoitussuojattu.

## Yleiset esimerkit
Pakkaa tiedosto nimeltä `esimerkki.txt`:
```bash
gzip esimerkki.txt
```

Purkaa pakattu tiedosto nimeltä `esimerkki.txt.gz`:
```bash
gzip -d esimerkki.txt.gz
```

Pakkaa tiedosto ja säilytä alkuperäinen:
```bash
gzip -k esimerkki.txt
```

Näytä pakkausprosessin yksityiskohtia:
```bash
gzip -v esimerkki.txt
```

Pakataan tiedosto pakkaamalla se, vaikka se olisi jo pakattu:
```bash
gzip -f esimerkki.txt.gz
```

## Vinkit
- Käytä `-k`-vaihtoehtoa, jos haluat säilyttää alkuperäiset tiedostot pakkaamisen jälkeen.
- Tarkista pakattujen tiedostojen koko käyttämällä `ls -lh` -komentoa.
- Muista, että `gzip` ei voi pakata hakemistoja suoraan; käytä `tar`-komentoa hakemistojen pakkaamiseen ennen `gzip`-komentoa.