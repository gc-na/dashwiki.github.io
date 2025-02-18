# [Suomi] Debian Almquist Shell (dash) sftp käyttö: Tiedostojen siirtäminen turvallisesti

## Yleiskatsaus
`sftp` (Secure File Transfer Protocol) on komento, jota käytetään tiedostojen siirtämiseen turvallisesti SSH-yhteyden kautta. Se tarjoaa interaktiivisen käyttöliittymän, jonka avulla käyttäjät voivat siirtää tiedostoja paikallisten ja etäpalvelimien välillä.

## Käyttö
Perussyntaksi `sftp`-komennolle on seuraava:

```bash
sftp [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-o`: Määrittää vaihtoehtoja, kuten `Port`, `User`, jne.
- `-P`: Määrittää etäpalvelimen portin.
- `-v`: Näyttää yksityiskohtaisia tietoja yhteyden muodostamisesta ja siirroista.

## Yleiset esimerkit
### Yhteyden muodostaminen etäpalvelimeen
```bash
sftp käyttäjä@etäpalvelin
```

### Tiedoston lataaminen etäpalvelimelta
```bash
sftp käyttäjä@etäpalvelin:getti/tiedosto.txt
```

### Tiedoston lähettäminen etäpalvelimelle
```bash
sftp käyttäjä@etäpalvelin:lähetä/tiedosto.txt
```

### Kaikkien tiedostojen listaaminen etäpalvelimella
```bash
sftp käyttäjä@etäpalvelin
ls
```

### Tiedoston poistaminen etäpalvelimelta
```bash
sftp käyttäjä@etäpalvelin
rm tiedosto.txt
```

## Vinkit
- Käytä `-v`-vaihtoehtoa virheiden vianetsintään, jos yhteys ei toimi odotetusti.
- Varmista, että SSH-avain on määritetty oikein, jotta voit muodostaa yhteyden ilman salasanaa.
- Hyödynnä `lcd`-komentoa, jolla voit vaihtaa paikallista työskentelyhakemistoa ennen tiedostojen siirtämistä.