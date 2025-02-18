# [Suomi] Debian Almquist Shell (dash) date: [näyttää ja muokkaa päivämäärää ja aikaa]

## Overview
`date`-komento näyttää nykyisen päivämäärän ja ajan tai muokkaa niitä halutun muotoiseksi. Se on hyödyllinen työkalu aikaleimojen käsittelyssä ja aikavyöhykkeiden hallinnassa.

## Usage
Perussyntaksi `date`-komennolle on seuraava:

```bash
date [options] [arguments]
```

## Common Options
- `-u`: Näyttää UTC-aikavyöhykkeen mukaisen päivämäärän ja ajan.
- `+FORMAT`: Määrittää tulostettavan päivämäärän ja ajan muodon.
- `-d STRING`: Näyttää päivämäärän ja ajan, joka vastaa annettua merkkijonoa.
- `-s STRING`: Asettaa järjestelmän päivämääräksi ja ajaksi annetun merkkijonon mukaisesti.

## Common Examples
1. Nykyisen päivämäärän ja ajan näyttäminen:
   ```bash
   date
   ```

2. Päivämäärän ja ajan näyttäminen UTC-aikavyöhykkeellä:
   ```bash
   date -u
   ```

3. Erityisen muotoisen päivämäärän näyttäminen:
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

4. Tulevan päivämäärän näyttäminen:
   ```bash
   date -d "next Friday"
   ```

5. Järjestelmän päivämäärän ja ajan asettaminen:
   ```bash
   date -s "2023-10-01 12:00:00"
   ```

## Tips
- Käytä `+FORMAT`-vaihtoehtoa, jotta saat päivämäärän ja ajan juuri haluamassasi muodossa.
- Muista, että järjestelmän päivämäärän ja ajan muuttaminen vaatii yleensä pääkäyttäjän oikeudet.
- Voit käyttää `man date` saadaksesi lisätietoja ja nähdäksesi kaikki käytettävissä olevat vaihtoehdot.