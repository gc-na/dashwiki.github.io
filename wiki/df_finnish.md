# [Suomi] Debian Almquist Shell (dash) df käyttö: Näyttää tiedostojärjestelmän levytilan

## Yleiskatsaus
`df`-komento näyttää tiedostojärjestelmän käytettävissä olevan ja käytetyn levytilan. Se on hyödyllinen työkalu, kun halutaan tarkistaa, kuinka paljon tilaa on jäljellä eri tiedostojärjestelmissä.

## Käyttö
Perussyntaksi `df`-komennolle on seuraava:
```bash
df [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`: Näyttää tiedostojärjestelmän koon ihmislukuisessa muodossa (esim. KB, MB, GB).
- `-T`: Näyttää tiedostojärjestelmän tyypin.
- `-a`: Näyttää myös nollatilassa olevat tiedostojärjestelmät.
- `-i`: Näyttää inodejen käytön sen sijaan, että näyttäisi levytilan käytön.

## Yleiset esimerkit
1. Näytä kaikki tiedostojärjestelmät ja niiden käyttö:
    ```bash
    df
    ```

2. Näytä tiedostojärjestelmät ihmislukuisessa muodossa:
    ```bash
    df -h
    ```

3. Näytä tiedostojärjestelmien tyypit:
    ```bash
    df -T
    ```

4. Näytä inodejen käyttö:
    ```bash
    df -i
    ```

5. Näytä kaikki tiedostojärjestelmät, mukaan lukien tyhjät:
    ```bash
    df -a
    ```

## Vinkit
- Käytä `-h`-vaihtoehtoa saadaksesi helposti luettavaa tietoa levytilasta.
- Säännöllinen tarkistus `df`-komennolla voi auttaa ennakoimaan levytilan loppumista.
- Voit yhdistää `df`-komennon muiden komentojen kanssa, kuten `grep`, suodattaaksesi tietoa tiettyjen tiedostojärjestelmien osalta. Esimerkiksi:
    ```bash
    df -h | grep /dev/sda1
    ```