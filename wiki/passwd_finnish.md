# [Suomi] Debian Almquist Shell (dash) passwd käyttö: Salasanan hallinta

## Yleiskatsaus
`passwd`-komento käytetään käyttäjätilin salasanan muuttamiseen tai hallintaan. Sen avulla voit vaihtaa oman tai toisen käyttäjän salasanan, mikä on tärkeää järjestelmän turvallisuuden kannalta.

## Käyttö
Perussyntaksi `passwd`-komennolle on seuraava:
```
passwd [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`: Poistaa käyttäjän salasanan.
- `-l`: Lukitsee käyttäjätilin, jolloin käyttäjä ei voi kirjautua sisään.
- `-u`: Vapauttaa lukitun käyttäjätilin.
- `-e`: Pakottaa käyttäjän vaihtamaan salasanan seuraavalla kirjautumiskerralla.

## Yleiset esimerkit
- Oman salasanan vaihtaminen:
  ```bash
  passwd
  ```
  Tämä komento kysyy nykyistä salasanaa ja pyytää syöttämään uuden salasanan.

- Toisen käyttäjän salasanan vaihtaminen (vaatii pääkäyttäjän oikeudet):
  ```bash
  sudo passwd käyttäjänimi
  ```
  Korvaa `käyttäjänimi` haluamallasi käyttäjänimellä.

- Käyttäjän salasanan poistaminen:
  ```bash
  sudo passwd -d käyttäjänimi
  ```

- Käyttäjätilin lukitseminen:
  ```bash
  sudo passwd -l käyttäjänimi
  ```

- Käyttäjätilin vapauttaminen:
  ```bash
  sudo passwd -u käyttäjänimi
  ```

## Vinkit
- Varmista, että uusi salasana on tarpeeksi vahva, sisältäen sekä isoja että pieniä kirjaimia, numeroita ja erikoismerkkejä.
- Käytä `passwd`-komentoa säännöllisesti varmistaaksesi, että käyttäjätilit ovat suojattuja.
- Muista, että salasanan vaihtaminen voi vaikuttaa käyttäjän pääsyyn järjestelmään, joten käytä komentoja varoen.