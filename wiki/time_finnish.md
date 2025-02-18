# [Suomi] Debian Almquist Shell (dash) time käyttö: Ajan mittaaminen komentoille

## Yleiskatsaus
`time`-komento mittaa ja raportoi aikaa, joka kuluu tietyn komennon suorittamiseen. Se antaa tietoa sekä käyttäjäajasta että järjestelmäajasta, mikä auttaa käyttäjiä optimoimaan skriptejä ja komentoja.

## Käyttö
Perussyntaksi `time`-komennolle on seuraava:

```bash
time [options] [arguments]
```

## Yleiset vaihtoehdot
- `-p`: Tulostaa ajan POSIX-yhteensopivassa muodossa.
- `-o <tiedosto>`: Tallentaa ajan tuloksen määritettyyn tiedostoon.
- `-v`: Näyttää yksityiskohtaisemman raportin ajasta ja resursseista.

## Yleiset esimerkit
1. Perusajan mittaus:
   ```bash
   time ls -l
   ```

2. Ajan tallentaminen tiedostoon:
   ```bash
   time -o aika.txt sleep 2
   ```

3. Yksityiskohtaisen raportin näyttäminen:
   ```bash
   time -v find / -name "example.txt"
   ```

4. Ajan mittaaminen skriptin suorittamiseen:
   ```bash
   time ./my_script.sh
   ```

## Vinkit
- Käytä `-p`-vaihtoehtoa, jos tarvitset tuloksen POSIX-yhteensopivassa muodossa.
- Tallenna tulokset tiedostoon, jos haluat analysoida useita suorituksia myöhemmin.
- Yksityiskohtainen raportti (`-v`) voi olla hyödyllinen, kun haluat ymmärtää resurssien käyttöä tarkemmin.