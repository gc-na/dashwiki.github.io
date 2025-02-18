# [Suomi] Debian Almquist Shell (dash) crontab käyttö: Aikatauluta komentoja

## Yleiskatsaus
`crontab`-komento on työkalu, jota käytetään aikatauluttamaan komentoja tai skriptejä suoritettavaksi tietyin aikavälein. Se on erityisen hyödyllinen toistuvien tehtävien automatisoimisessa, kuten varmuuskopioinnissa tai järjestelmän ylläpidossa.

## Käyttö
Perussyntaksi `crontab`-komennolle on seuraava:

```bash
crontab [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e`: Muokkaa nykyistä crontab-tiedostoa.
- `-l`: Näytä nykyinen crontab-tiedosto.
- `-r`: Poista nykyinen crontab-tiedosto.
- `-i`: Vahvista ennen crontab-tiedoston poistamista.

## Yleiset esimerkit
### 1. Aikatauluta komento joka päivä klo 2:00
```bash
0 2 * * * /polku/komento
```

### 2. Aikatauluta skripti joka maanantai klo 3:30
```bash
30 3 * * 1 /polku/skripti.sh
```

### 3. Näytä nykyinen crontab
```bash
crontab -l
```

### 4. Muokkaa nykyistä crontab-tiedostoa
```bash
crontab -e
```

### 5. Poista nykyinen crontab
```bash
crontab -r
```

## Vinkit
- Varmista, että skriptisi ovat suoritettavissa ja että niillä on oikeat käyttöoikeudet.
- Käytä täydellisiä polkuja komentoihin ja skripteihin, jotta vältät mahdolliset virheet.
- Testaa komentoasi manuaalisesti ennen aikatauluttamista varmistaaksesi, että se toimii odotetusti.