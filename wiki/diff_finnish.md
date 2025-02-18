# [Suomi] Debian Almquist Shell (dash) diff käyttö: vertaa tiedostoja

## Yleiskatsaus
`diff`-komento vertailee kahta tiedostoa ja näyttää niiden väliset erot. Tämä on erityisen hyödyllistä ohjelmoinnissa ja tiedostojen hallinnassa, kun halutaan nähdä, mitä muutoksia on tehty.

## Käyttö
Perussyntaksi `diff`-komennolle on seuraava:

```bash
diff [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-u`: Näyttää eron "unified" muodossa, joka on helpompi lukea.
- `-i`: Ignoroi kirjainkoolla eroja.
- `-w`: Ignoroi tyhjät merkit.
- `-b`: Ignoroi tyhjien merkkien muutokset.

## Yleiset esimerkit
1. **Perusvertailu kahden tiedoston välillä:**
   ```bash
   diff tiedosto1.txt tiedosto2.txt
   ```

2. **Unified-muotoisen eron näyttäminen:**
   ```bash
   diff -u tiedosto1.txt tiedosto2.txt
   ```

3. **Kirjainkoolla erojen sivuuttaminen:**
   ```bash
   diff -i tiedosto1.txt tiedosto2.txt
   ```

4. **Tyhjien merkkien muutosten sivuuttaminen:**
   ```bash
   diff -w tiedosto1.txt tiedosto2.txt
   ```

## Vinkit
- Käytä `-u`-vaihtoehtoa, kun haluat jakaa eron muille, sillä se on helpompi lukea.
- Voit ohjata `diff`-komennon tulosteen tiedostoon käyttämällä `>`-merkkiä, esimerkiksi:
  ```bash
  diff tiedosto1.txt tiedosto2.txt > erot.txt
  ```
- Hyödynnä `diff`-komentoa yhdessä `patch`-komennon kanssa, jos haluat soveltaa eroja tiedostoihin.