# [Suomi] Debian Almquist Shell (dash) tar käyttö: Tiedostojen pakkaaminen ja purkaminen

## Yleiskatsaus
`tar`-komento on työkalu, jota käytetään tiedostojen pakkaamiseen ja purkamiseen Unix- ja Linux-järjestelmissä. Se mahdollistaa useiden tiedostojen yhdistämisen yhdeksi arkistoksi, mikä helpottaa tiedostojen siirtämistä ja varmuuskopiointia.

## Käyttö
Perussyntaksi `tar`-komennolle on seuraava:

```bash
tar [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Luo uusi arkisto.
- `-x`: Purkaa arkiston.
- `-f`: Määrittää arkiston nimen.
- `-v`: Näyttää prosessin aikana käsiteltävät tiedostot (verbose).
- `-z`: Pakkaa tai purkaa tiedostoja gzip-muodossa.
- `-j`: Pakkaa tai purkaa tiedostoja bzip2-muodossa.

## Yleiset esimerkit

### Arkiston luominen
Luo arkisto nimeltä `esimerkki.tar` ja lisää siihen tiedostot `tiedosto1.txt` ja `tiedosto2.txt`:
```bash
tar -cvf esimerkki.tar tiedosto1.txt tiedosto2.txt
```

### Arkiston purkaminen
Purkaa arkisto `esimerkki.tar` nykyiseen hakemistoon:
```bash
tar -xvf esimerkki.tar
```

### Gzip-pakatun arkiston luominen
Luo gzip-pakatun arkiston nimeltä `esimerkki.tar.gz`:
```bash
tar -czvf esimerkki.tar.gz tiedosto1.txt tiedosto2.txt
```

### Bzip2-pakatun arkiston purkaminen
Purkaa bzip2-pakattu arkisto `esimerkki.tar.bz2`:
```bash
tar -xjvf esimerkki.tar.bz2
```

## Vinkit
- Käytä `-v`-vaihtoehtoa, jotta näet, mitkä tiedostot käsitellään, mikä voi olla hyödyllistä suurissa arkistoissa.
- Varmista, että käytät oikeaa pakkausmuotoa (gzip tai bzip2) tarpeidesi mukaan.
- Testaa arkiston eheys ennen purkamista käyttämällä `-t`-vaihtoehtoa, esimerkiksi `tar -tvf esimerkki.tar`.