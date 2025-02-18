# [Suomi] Debian Almquist Shell (dash) env käyttö: Ympäristömuuttujien hallinta

## Yleiskatsaus
`env`-komento on työkalu, jota käytetään ympäristömuuttujien näyttämiseen tai muokkaamiseen ennen toisen komennon suorittamista. Se mahdollistaa ympäristön muuttujien asettamisen tai poistamisen, mikä voi olla hyödyllistä ohjelmien tai skriptien suorittamisessa tietyissä ympäristöissä.

## Käyttö
Perussyntaksi `env`-komennolle on seuraava:

```sh
env [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-i`, `--ignore-environment`: Suorittaa komennon tyhjällä ympäristöllä, ilman olemassa olevia ympäristömuuttujia.
- `-u VAR`, `--unset=VAR`: Poistaa määritellyn ympäristömuuttujan ennen komennon suorittamista.
- `VAR=value`: Asettaa ympäristömuuttujan ennen komennon suorittamista.

## Yleiset esimerkit
1. **Näytä nykyiset ympäristömuuttujat:**
   ```sh
   env
   ```

2. **Suorita komento tietyllä ympäristömuuttujalla:**
   ```sh
   env MY_VAR=1234 bash -c 'echo $MY_VAR'
   ```

3. **Poista ympäristömuuttuja ennen komennon suorittamista:**
   ```sh
   env -u MY_VAR bash -c 'echo $MY_VAR'
   ```

4. **Suorita komento tyhjällä ympäristöllä:**
   ```sh
   env -i bash -c 'echo $HOME'
   ```

## Vinkit
- Käytä `env`-komentoa, kun haluat testata ohjelmia tai skriptejä ilman häiriöitä nykyisistä ympäristömuuttujista.
- Varmista, että ymmärrät, mitä ympäristömuuttujia tarvitset, kun asetat niitä `env`-komennolla, jotta vältät mahdolliset virheet.
- Hyödynnä `env`-komentoa skripteissä, joissa haluat varmistaa, että tietyt muuttujat ovat määriteltyjä ennen ohjelman suorittamista.