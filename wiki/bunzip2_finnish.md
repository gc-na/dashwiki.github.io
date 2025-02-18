# [Suomi] Debian Almquist Shell (dash) bunzip2 käyttö: Tiedostojen purkaminen

## Yleiskatsaus
`bunzip2` on komento, jota käytetään Bzip2-pakkauksen purkamiseen. Se ottaa vastaan Bzip2-muotoisia tiedostoja ja purkaa ne alkuperäiseen muotoonsa.

## Käyttö
Perussyntaksi komennolle on seuraava:

```bash
bunzip2 [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-k`: Säilyttää alkuperäisen pakatun tiedoston purkamisen jälkeen.
- `-f`: Pakottaa purkamisen, vaikka tiedostoja olisi jo olemassa.
- `-v`: Näyttää yksityiskohtaisempaa tietoa purkamisprosessista.

## Yleiset esimerkit
### Peruspurku
Purkaa tiedoston `esimerkki.bz2`:
```bash
bunzip2 esimerkki.bz2
```

### Tiedoston säilyttäminen
Purkaa tiedoston `esimerkki.bz2`, mutta säilyttää alkuperäisen tiedoston:
```bash
bunzip2 -k esimerkki.bz2
```

### Pakottaminen
Pakottaa purkamaan tiedoston `esimerkki.bz2`, vaikka tiedosto `esimerkki` on jo olemassa:
```bash
bunzip2 -f esimerkki.bz2
```

### Yksityiskohtainen tieto
Näyttää purkamisprosessin yksityiskohtia tiedostosta `esimerkki.bz2`:
```bash
bunzip2 -v esimerkki.bz2
```

## Vinkit
- Varmista, että sinulla on riittävästi levytilaa ennen purkamista, sillä purkaminen luo uuden tiedoston.
- Käytä `-k`-vaihtoehtoa, jos haluat säilyttää alkuperäisen pakatun tiedoston varmuuden vuoksi.
- Tarkista purkamisen jälkeen tiedoston eheys käyttämällä `file`-komentoa varmistaaksesi, että se on oikeassa muodossa.