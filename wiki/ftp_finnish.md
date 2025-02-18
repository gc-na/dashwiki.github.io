# [Suomi] Debian Almquist Shell (dash) ftp käyttö: Tiedostojen siirto

## Yleiskatsaus
`ftp`-komento on käytettävissä tiedostojen siirtämiseen tietokoneiden välillä Internetin tai paikallisten verkkojen kautta. Se mahdollistaa käyttäjien yhteyden muodostamisen FTP-palvelimiin, joista he voivat ladata tai lähettää tiedostoja.

## Käyttö
Perussyntaksi `ftp`-komennolle on seuraava:

```
ftp [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-v`: Näyttää vain virheviestit.
- `-n`: Estää automaattisen kirjautumisen.
- `-g`: Estää globaalit merkinnät.
- `-i`: Estää interaktiivisen tilan, jolloin tiedostot siirretään ilman vahvistusta.

## Yleiset esimerkit
### Yhteyden muodostaminen FTP-palvelimeen
```
ftp ftp.example.com
```

### Tiedoston lataaminen palvelimelta
```
get tiedosto.txt
```

### Tiedoston lähettäminen palvelimelle
```
put paikallinen_tiedosto.txt
```

### Kaikkien tiedostojen listaaminen palvelimella
```
ls
```

### Tiedoston poistaminen palvelimelta
```
delete tiedosto.txt
```

## Vinkit
- Käytä `-n`-vaihtoehtoa, jos et halua automaattista kirjautumista, erityisesti julkisilla palvelimilla.
- Muista tarkistaa tiedostojen oikeudet ennen niiden poistamista tai muokkaamista.
- Hyödynnä `ls`-komentoa tiedostojen tarkistamiseen ennen siirtoja, jotta tiedät, mitä tiedostoja on saatavilla.