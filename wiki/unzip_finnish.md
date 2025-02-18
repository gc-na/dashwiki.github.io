# [Suomi] Debian Almquist Shell (dash) unzip käyttö: Pakettien purkaminen

## Yleiskatsaus
`unzip`-komento on työkalu, jota käytetään ZIP-tiedostojen purkamiseen. Se mahdollistaa pakattujen tiedostojen sisällön tarkastelun ja tiedostojen erottamisen alkuperäisestä ZIP-arkistosta.

## Käyttö
Perussyntaksi `unzip`-komennolle on seuraava:

```bash
unzip [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Listaa ZIP-arkiston sisällön ilman purkamista.
- `-o`: Ylikirjoittaa olemassa olevat tiedostot ilman kyselyä.
- `-d [hakemisto]`: Määrittää hakemiston, johon tiedostot puretaan.
- `-q`: Hiljainen tila, ei näytä purkamisen edistymistä.

## Yleiset esimerkit
### 1. ZIP-tiedoston purkaminen nykyiseen hakemistoon
```bash
unzip tiedosto.zip
```

### 2. ZIP-tiedoston sisällön listaaminen
```bash
unzip -l tiedosto.zip
```

### 3. Tiedostojen purkaminen tiettyyn hakemistoon
```bash
unzip tiedosto.zip -d /polku/hakemistoon
```

### 4. Olemassa olevien tiedostojen ylikirjoittaminen
```bash
unzip -o tiedosto.zip
```

## Vinkit
- Käytä `-q`-vaihtoehtoa, jos haluat purkaa tiedostoja ilman ylimääräistä tulostusta, mikä voi olla hyödyllistä skripteissä.
- Varmista, että sinulla on tarvittavat oikeudet hakemistoon, johon tiedostot puretaan.
- Tarkista aina ZIP-arkiston sisältö ennen purkamista `-l`-vaihtoehdolla, jotta tiedät, mitä tiedostoja olet purkamassa.