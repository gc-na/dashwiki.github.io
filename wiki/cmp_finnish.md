# [Suomi] Debian Almquist Shell (dash) cmp käyttö: Tiedostojen vertailu

## Yleiskatsaus
`cmp`-komento vertaa kahta tiedostoa ja ilmoittaa, ovatko ne samat vai eivät. Jos tiedostot eroavat, komento näyttää ensimmäisen eron sijainnin.

## Käyttö
Perussyntaksi `cmp`-komennolle on seuraava:
```
cmp [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Näyttää kaikki eroavaisuudet tavu kerrallaan.
- `-s`: Ei tulosta mitään, vaan palauttaa vain eron tilan.
- `-i N`: Ohittaa ensimmäiset N tavua ennen vertailua.

## Yleiset esimerkit
- Vertaa kahta tiedostoa:
  ```bash
  cmp tiedosto1.txt tiedosto2.txt
  ```

- Käytä `-s`-vaihtoehtoa tarkistaaksesi, ovatko tiedostot samat ilman tulostusta:
  ```bash
  cmp -s tiedosto1.txt tiedosto2.txt
  ```

- Näytä kaikki eroavaisuudet tavu kerrallaan:
  ```bash
  cmp -l tiedosto1.txt tiedosto2.txt
  ```

- Ohita ensimmäiset 10 tavua ennen vertailua:
  ```bash
  cmp -i 10 tiedosto1.txt tiedosto2.txt
  ```

## Vinkit
- Käytä `-s`-vaihtoehtoa, kun haluat vain tietää, ovatko tiedostot samat ilman ylimääräistä tulostusta.
- `cmp` on hyödyllinen työkalu skripteissä, joissa tiedostojen vertailu on tarpeen.
- Muista, että `cmp` vertaa tiedostoja tavu kerrallaan, joten se on tarkempi kuin monet muut vertailumenetelmät.