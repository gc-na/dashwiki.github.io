# [Suomi] Debian Almquist Shell (dash) free: Muistin käytön tarkastelu

## Overview
`free`-komento näyttää järjestelmän muistin käytön tilan. Se antaa tietoa käytettävissä olevasta, käytetystä ja vapaasta muistista sekä välimuistista ja swap-tilasta.

## Usage
Perussyntaksi `free`-komennolle on seuraava:

```bash
free [options] [arguments]
```

## Common Options
- `-h`, `--human`: Näyttää muistimäärät ihmislukemassa muodossa (esim. KB, MB, GB).
- `-m`: Näyttää muistimäärät megatavuina.
- `-g`: Näyttää muistimäärät gigatavuina.
- `-s <sekunnit>`: Päivittää näyttöä tietyin aikavälein.
- `-t`: Näyttää yhteenvetotiedot.

## Common Examples

1. Perusmuistin tila:
   ```bash
   free
   ```

2. Muistin tila ihmislukemassa muodossa:
   ```bash
   free -h
   ```

3. Muistin tila megatavuina:
   ```bash
   free -m
   ```

4. Muistin tila gigatavuina:
   ```bash
   free -g
   ```

5. Muistin tila päivittyen 5 sekunnin välein:
   ```bash
   free -s 5
   ```

6. Yhteenvetotiedot muistin käytöstä:
   ```bash
   free -t
   ```

## Tips
- Käytä `-h`-vaihtoehtoa saadaksesi helposti luettavaa tietoa muistista.
- Voit yhdistää `free`-komennon `watch`-komentoon, jolloin saat jatkuvasti päivittyvää tietoa muistista:
  ```bash
  watch free -h
  ```
- Tarkista muistin käyttö säännöllisesti, erityisesti järjestelmän suorituskyvyn optimoinnin yhteydessä.