# [Suomi] Debian Almquist Shell (dash) head käyttö: Näytä tiedoston alkuosa

## Yleiskatsaus
`head`-komento näyttää tiedoston ensimmäiset rivit. Se on hyödyllinen, kun haluat nopeasti tarkastella tiedoston sisältöä ilman, että sinun tarvitsee avata koko tiedostoa.

## Käyttö
Perussyntaksi `head`-komennolle on seuraava:

```bash
head [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n [numero]`: Määrittää näytettävien rivien määrän. Oletuksena näytetään 10 riviä.
- `-c [tavua]`: Näyttää määritetyn määrän tavuja tiedoston alusta.
- `-q`: Ei tulosta tiedoston nimeä ennen sen sisältöä, kun useita tiedostoja käsitellään.

## Yleiset esimerkit
1. Näytä ensimmäiset 10 riviä tiedostosta `esimerkki.txt`:
   ```bash
   head esimerkki.txt
   ```

2. Näytä ensimmäiset 5 riviä tiedostosta `data.txt`:
   ```bash
   head -n 5 data.txt
   ```

3. Näytä ensimmäiset 20 tavua tiedostosta `tiedosto.bin`:
   ```bash
   head -c 20 tiedosto.bin
   ```

4. Näytä useiden tiedostojen ensimmäiset 10 riviä kerralla:
   ```bash
   head tiedosto1.txt tiedosto2.txt
   ```

## Vinkit
- Käytä `-n`-vaihtoehtoa, jos haluat tarkastella eri määrää rivejä kuin oletusarvoinen 10.
- Voit yhdistää `head`-komennon putkessa muiden komentojen kanssa, esimerkiksi `tail`, saadaksesi tarkempaa tietoa tiedoston sisällöstä.
- Hyödynnä `head`-komentoa suurten lokitiedostojen tarkastelussa, jotta saat nopeasti käsityksen niiden sisällöstä ilman, että lataat koko tiedostoa.