# [Suomi] Debian Almquist Shell (dash) zip käyttö: Tiedostojen pakkaaminen

## Yleiskatsaus
`zip`-komento on työkalu, jota käytetään tiedostojen ja kansioiden pakkaamiseen zip-muotoon. Se auttaa vähentämään tiedostojen kokoa ja tekee niiden jakamisesta helpompaa.

## Käyttö
Perussyntaksi `zip`-komennolle on seuraava:

```bash
zip [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-r`: Pakkaa hakemiston ja sen sisällön rekursiivisesti.
- `-e`: Luo salattu zip-tiedosto, joka vaatii salasanan purkamiseen.
- `-9`: Käytä maksimaalista pakkaustasoa.
- `-d`: Poistaa tiedostoja zip-arkistosta.

## Yleiset esimerkit
Pakkaa yksi tiedosto zip-tiedostoon:

```bash
zip tiedosto.zip tiedosto.txt
```

Pakkaa useita tiedostoja zip-tiedostoon:

```bash
zip tiedosto.zip tiedosto1.txt tiedosto2.txt
```

Pakkaa koko hakemisto rekursiivisesti:

```bash
zip -r hakemisto.zip hakemisto/
```

Luo salattu zip-tiedosto:

```bash
zip -e salattu.zip tiedosto.txt
```

Poista tiedosto zip-arkistosta:

```bash
zip -d tiedosto.zip tiedosto.txt
```

## Vinkit
- Käytä `-9`-vaihtoehtoa, jos tiedostojen koko on erityisen tärkeä ja haluat maksimoida pakkaustehon.
- Muista, että salattu zip-tiedosto voi olla turvallinen tapa jakaa arkaluontoista tietoa, mutta varmista, että salasana on vahva.
- Tarkista zip-arkiston sisältö komennolla `unzip -l tiedosto.zip` ennen sen purkamista varmistaaksesi, että se sisältää odotetut tiedostot.