# [Suomi] Debian Almquist Shell (dash) uniq käyttö: Poistaa peräkkäiset duplikaatit

## Yleiskatsaus
`uniq`-komento on työkalu, joka poistaa peräkkäiset duplikaatit tiedostosta tai syötteestä. Se on erityisen hyödyllinen, kun halutaan tiivistää tietoa tai analysoida dataa, jossa on toistuvia rivejä.

## Käyttö
Perussyntaksi `uniq`-komennolle on seuraava:

```bash
uniq [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Laskee ja näyttää duplikaattirivien määrän.
- `-d`: Näyttää vain ne rivit, jotka ovat toistuvia.
- `-u`: Näyttää vain ne rivit, jotka ovat ainutlaatuisia.
- `-i`: Ohittaa suur- ja pienikirjaimisuuden vertailussa.

## Yleiset esimerkit
1. Poista peräkkäiset duplikaatit tiedostosta:
   ```bash
   uniq tiedosto.txt
   ```

2. Laske duplikaattirivien määrä:
   ```bash
   uniq -c tiedosto.txt
   ```

3. Näytä vain toistuvat rivit:
   ```bash
   uniq -d tiedosto.txt
   ```

4. Näytä vain ainutlaatuiset rivit:
   ```bash
   uniq -u tiedosto.txt
   ```

5. Ohita suur- ja pienikirjaimisuus:
   ```bash
   uniq -i tiedosto.txt
   ```

## Vinkit
- Varmista, että syöte on lajiteltu ennen `uniq`-komennon käyttöä, sillä se poistaa vain peräkkäiset duplikaatit.
- Voit yhdistää `uniq`-komennon muihin komentoihin, kuten `sort`, saadaksesi haluamasi tulokset:
  ```bash
  sort tiedosto.txt | uniq
  ```
- Käytä `-c`-vaihtoehtoa, jos haluat nopeasti nähdä, kuinka monta kertaa kukin rivi toistuu, mikä voi olla hyödyllistä datan analysoinnissa.