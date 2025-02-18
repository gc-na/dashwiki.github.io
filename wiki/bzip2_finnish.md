# [Suomi] Debian Almquist Shell (dash) bzip2 käyttö: Tiedostojen pakkaaminen

## Yleiskatsaus
bzip2 on komento, jota käytetään tiedostojen pakkaamiseen tehokkaasti. Se vähentää tiedostojen kokoa käyttämällä bzip2-pakkausalgoritmia, mikä tekee siitä erinomaisen valinnan suurten tiedostojen käsittelyyn.

## Käyttö
Perussyntaksi bzip2-komennolle on seuraava:

```
bzip2 [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`, `--decompress`: Purkaa pakatut tiedostot.
- `-k`, `--keep`: Säilyttää alkuperäisen tiedoston pakkaamisen jälkeen.
- `-f`, `--force`: Pakkaa tai purkaa tiedostot, vaikka ne olisivat jo olemassa.
- `-v`, `--verbose`: Näyttää lisätietoja pakkausprosessista.

## Yleiset esimerkit
Pakkaaminen:

```bash
bzip2 tiedosto.txt
```

Pakkaa `tiedosto.txt` ja luo `tiedosto.txt.bz2`.

Purkaminen:

```bash
bzip2 -d tiedosto.txt.bz2
```

Purkaa `tiedosto.txt.bz2` ja palauttaa alkuperäisen `tiedosto.txt` tiedoston.

Pakkaaminen säilyttäen alkuperäinen tiedosto:

```bash
bzip2 -k tiedosto.txt
```

Pakkaa `tiedosto.txt` ja säilyttää alkuperäisen tiedoston.

Pakettien pakkaaminen useista tiedostoista:

```bash
bzip2 tiedosto1.txt tiedosto2.txt
```

Pakkaa molemmat tiedostot ja luo `tiedosto1.txt.bz2` ja `tiedosto2.txt.bz2`.

## Vinkit
- Käytä `-v`-vaihtoehtoa, jos haluat nähdä pakkausprosessin edistymisen.
- Muista käyttää `-k`-vaihtoehtoa, jos haluat säilyttää alkuperäiset tiedostot pakkaamisen jälkeen.
- Bzip2 on erityisen tehokas suurten tekstimuotoisten tiedostojen pakkaamisessa, joten kokeile sitä suurilla tiedostoilla saadaksesi parhaat tulokset.