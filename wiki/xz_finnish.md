# [Suomi] Debian Almquist Shell (dash) xz käyttö: Tiedostojen pakkaaminen ja purkaminen

## Yleiskatsaus
`xz` on komento, jota käytetään tiedostojen pakkaamiseen ja purkamiseen tehokkaasti. Se käyttää XZ-pakkausalgoritmia, joka tarjoaa korkean pakkaussuhteen ja on erityisen hyödyllinen suurten tiedostojen käsittelyssä.

## Käyttö
Perussyntaksi komennolle on seuraava:
```
xz [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`, `--decompress`: Purkaa pakatun tiedoston.
- `-k`, `--keep`: Säilyttää alkuperäisen tiedoston pakkaamisen jälkeen.
- `-v`, `--verbose`: Näyttää yksityiskohtaisempaa tietoa pakkausprosessista.
- `-9`: Käyttää maksimaalista pakkausastetta, mikä voi hidastaa prosessia mutta tuottaa pienempiä tiedostoja.

## Yleiset esimerkit
Pakkaaminen:
```bash
xz tiedosto.txt
```
Tämä komento pakkaa `tiedosto.txt` ja luo `tiedosto.txt.xz` -tiedoston.

Purkaminen:
```bash
xz -d tiedosto.txt.xz
```
Tämä komento purkaa `tiedosto.txt.xz` -tiedoston ja palauttaa alkuperäisen `tiedosto.txt` -tiedoston.

Pakkaaminen säilyttäen alkuperäinen tiedosto:
```bash
xz -k tiedosto.txt
```
Tässä komennossa `tiedosto.txt` pakataan, mutta alkuperäinen tiedosto jää voimaan.

Yksityiskohtaisemman tiedon näyttäminen:
```bash
xz -v tiedosto.txt
```
Tämä komento näyttää pakkausprosessin aikana tietoa, kuten pakattujen tietojen koon.

## Vinkit
- Käytä `-9` -vaihtoehtoa vain, jos tiedostokoko on tärkeämpää kuin pakkausnopeus.
- Varmista, että sinulla on tarpeeksi levytilaa pakattujen tiedostojen tallentamiseen.
- Tarkista pakkausprosessin tulokset `-v` -vaihtoehdolla, jotta tiedät, kuinka tehokasta pakkaaminen oli.