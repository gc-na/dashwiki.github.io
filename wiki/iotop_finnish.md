# [Suomi] Debian Almquist Shell (dash) iotop käyttö: seuraa levy I/O:ta

## Overview
iotop on työkalu, joka näyttää reaaliaikaisesti, mitkä prosessit käyttävät eniten levy I/O:ta. Se on erityisen hyödyllinen järjestelmänvalvojille, jotka haluavat optimoida levyresurssien käyttöä ja tunnistaa mahdolliset pullonkaulat.

## Usage
Perussyntaksi iotop-komennolle on seuraava:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only` : Näyttää vain prosessit, jotka ovat tällä hetkellä käyttämässä levy I/O:ta.
- `-b`, `--batch` : Käynnistää iotopin erätilassa, jolloin se tulostaa tiedot ilman käyttöliittymää.
- `-d`, `--delay` : Määrittää viiveen sekunneissa tulosteen päivitykselle (oletus on 1 sekunti).
- `-p`, `--pid` : Seuraa vain tiettyä prosessia, jonka ID on annettu.

## Common Examples
Seuraavassa on muutamia käytännön esimerkkejä iotop-komennon käytöstä:

1. **Peruskomento iotopin käynnistämiseksi:**
   ```bash
   iotop
   ```

2. **Näytä vain prosessit, jotka käyttävät levy I/O:ta:**
   ```bash
   iotop -o
   ```

3. **Käynnistä iotop erätilassa ja tulosta tiedot 2 sekunnin välein:**
   ```bash
   iotop -b -d 2
   ```

4. **Seuraa tiettyä prosessia sen prosessi-ID:n mukaan:**
   ```bash
   iotop -p 1234
   ```

## Tips
- Käytä `-o`-vaihtoehtoa, jos haluat keskittyä vain aktiivisiin prosesseihin, mikä helpottaa ongelmien tunnistamista.
- Erätilassa (`-b`) voit ohjata tulosteen tiedostoon, mikä on hyödyllistä pitkäaikaisessa seurannassa.
- Muista, että iotop vaatii yleensä root-oikeudet toimiakseen oikein, joten käytä `sudo`-komentoa tarvittaessa.