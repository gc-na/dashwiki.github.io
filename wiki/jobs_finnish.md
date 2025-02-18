# [Suomi] Debian Almquist Shell (dash) jobs käyttö: Näyttää taustaprosessit

## Overview
`jobs`-komento näyttää nykyisessä kuorissa (shell) suoritetut taustaprosessit. Se tarjoaa tietoa prosessien tilasta, kuten onko ne käynnissä, pysäytetty tai lopetettu.

## Usage
Perussyntaksi `jobs`-komennolle on seuraava:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Näyttää prosessitunnukset (PID) jokaisen työn yhteydessä.
- `-n`: Näyttää vain ne työt, jotka ovat muuttaneet tilaansa viimeisen komennon jälkeen.
- `-p`: Näyttää vain prosessitunnukset.

## Common Examples
1. Näytä kaikki taustaprosessit:
   ```bash
   jobs
   ```

2. Näytä taustaprosessit prosessitunnuksilla:
   ```bash
   jobs -l
   ```

3. Näytä vain ne työt, jotka ovat muuttaneet tilaansa:
   ```bash
   jobs -n
   ```

4. Näytä vain prosessitunnukset:
   ```bash
   jobs -p
   ```

## Tips
- Käytä `bg`- ja `fg`-komentoja yhdessä `jobs`-komennon kanssa, jotta voit hallita taustaprosesseja tehokkaasti.
- Muista, että `jobs` näyttää vain nykyisen kuoren prosessit, joten varmista, että olet oikeassa kuorissa ennen komennon suorittamista.
- Hyödynnä `jobs`-komentoa virheiden ja prosessien hallinnan helpottamiseksi, erityisesti monimutkaisissa skripteissä.