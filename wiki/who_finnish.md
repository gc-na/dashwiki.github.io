# [Suomi] Debian Almquist Shell (dash) who: käyttäjätietojen näyttäminen

## Overview
`who`-komento näyttää tietoja kirjautuneista käyttäjistä järjestelmässä. Se tarjoaa tietoa käyttäjien nimistä, kirjautumisajoista ja muista tärkeistä tiedoista.

## Usage
Perussyntaksi `who`-komennolle on seuraava:

```
who [options] [arguments]
```

## Common Options
- `-b`: Näyttää järjestelmän viimeisimmän käynnistyspäivämäärän ja -ajan.
- `-q`: Näyttää vain kirjautuneiden käyttäjien nimet ja niiden lukumäärän.
- `-H`: Näyttää sarakeotsikot tulosteessa.

## Common Examples
1. Näytä kaikki kirjautuneet käyttäjät:
   ```bash
   who
   ```

2. Näytä järjestelmän viimeisin käynnistyspäivämäärä:
   ```bash
   who -b
   ```

3. Näytä vain käyttäjien nimet ja niiden lukumäärä:
   ```bash
   who -q
   ```

4. Näytä tuloste sarakeotsikoilla:
   ```bash
   who -H
   ```

## Tips
- Käytä `who`-komentoa yhdessä muiden komentojen, kuten `grep`, kanssa suodattaaksesi tietoja tietyistä käyttäjistä.
- Voit yhdistää `who`-komennon `wc -l`-komentoon saadaksesi kirjautuneiden käyttäjien kokonaismäärän:
  ```bash
  who | wc -l
  ```
- Muista, että `who` näyttää vain aktiiviset käyttäjät, joten se ei listaa käyttäjiä, jotka eivät ole kirjautuneina.