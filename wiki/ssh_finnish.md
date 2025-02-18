# [Suomi] Debian Almquist Shell (dash) ssh käyttö: Etäyhteyksien luominen

## Yleiskatsaus
`ssh` (Secure Shell) on protokolla, jota käytetään turvallisten etäyhteyksien luomiseen toiseen tietokoneeseen. Sen avulla voit kirjautua sisään etäpalvelimelle ja suorittaa komentoja turvallisesti salatun yhteyden kautta.

## Käyttö
Perussyntaksi `ssh`-komennolle on seuraava:

```bash
ssh [vaihtoehdot] [käyttäjä@isäntä]
```

## Yleiset vaihtoehdot
- `-p [portti]`: Määrittää yhteyden portin, jos se poikkeaa oletusportista (22).
- `-i [avain]`: Käyttää määritettyä yksityistä avainta autentikointiin.
- `-v`: Näyttää yksityiskohtaista tietoa yhteyden muodostamisesta (debugging).
- `-X`: Mahdollistaa X11-ikkunointijärjestelmän käytön etäyhteydessä.

## Yleiset esimerkit
### Yhteys etäpalvelimelle
Kirjaudu sisään etäpalvelimelle käyttäen oletusporttia:
```bash
ssh käyttäjä@esimerkki.com
```

### Yhteys eri porttiin
Kirjaudu sisään palvelimelle, joka kuuntelee eri portissa:
```bash
ssh -p 2222 käyttäjä@esimerkki.com
```

### Yksityisen avaimen käyttö
Kirjaudu sisään käyttäen erityistä yksityistä avainta:
```bash
ssh -i /polku/avain.pem käyttäjä@esimerkki.com
```

### Debugging-tietojen näyttäminen
Näytä yhteyden muodostamiseen liittyvät debug-tiedot:
```bash
ssh -v käyttäjä@esimerkki.com
```

### X11-ikkunointijärjestelmän käyttö
Mahdollista X11-ikkunointijärjestelmän käyttö etäyhteydessä:
```bash
ssh -X käyttäjä@esimerkki.com
```

## Vinkit
- Käytä `~/.ssh/config`-tiedostoa helpottamaan yhteyksien hallintaa ja määrittelyä.
- Varmista, että käytät vahvoja salasanoja tai avaimia turvallisuuden parantamiseksi.
- Hyödynnä SSH-tunnelointia suojattujen yhteyksien luomiseen paikallisten ja etäpalvelimien välillä.