# [Suomi] Debian Almquist Shell (dash) uname käyttö: Näyttää järjestelmän tiedot

## Yleiskatsaus
`uname`-komento on työkalu, jota käytetään Unix-tyyppisissä käyttöjärjestelmissä, kuten Debianissa, järjestelmän tiedon näyttämiseen. Se voi paljastaa tietoja kuten käyttöjärjestelmän nimen, version ja muita järjestelmään liittyviä tietoja.

## Käyttö
Perussyntaksi `uname`-komennolle on seuraava:

```bash
uname [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki saatavilla olevat tiedot.
- `-s`: Näyttää käyttöjärjestelmän nimen.
- `-n`: Näyttää verkon isäntänimen.
- `-r`: Näyttää käyttöjärjestelmän version.
- `-v`: Näyttää version lisätietoja.
- `-m`: Näyttää laitteiston arkkitehtuurin.
- `-p`: Näyttää prosessorin tyypin.
- `-i`: Näyttää laitteiston valmistajan.
- `-o`: Näyttää käyttöjärjestelmän nimen.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `uname`-komennon käytöstä:

1. Näytä kaikki tiedot:
   ```bash
   uname -a
   ```

2. Näytä vain käyttöjärjestelmän nimi:
   ```bash
   uname -s
   ```

3. Näytä käyttöjärjestelmän versio:
   ```bash
   uname -r
   ```

4. Näytä laitteiston arkkitehtuuri:
   ```bash
   uname -m
   ```

5. Näytä verkon isäntänimi:
   ```bash
   uname -n
   ```

## Vinkit
- Käytä `uname -a` saadaksesi kattavan yleiskuvan järjestelmästäsi yhdellä komennolla.
- Yhdistä `uname`-komento muihin komentoihin, kuten `grep`, suodataksesi tietoa tarkemmin.
- Muista, että `uname`-komennon tulokset voivat vaihdella eri järjestelmissä, joten kokeile eri vaihtoehtoja saadaksesi tarvitsemasi tiedot.