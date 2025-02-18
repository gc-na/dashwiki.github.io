# [Suomi] Debian Almquist Shell (dash) cal käyttö: Näyttää kalenterin

## Yleiskatsaus
`cal`-komento näyttää kalenterin valitulle kuukaudelle tai vuodelle. Se on hyödyllinen työkalu, kun haluat nopeasti tarkistaa päivämäärät tai nähdä, mihin viikonpäivään jokin päivä osuu.

## Käyttö
Perussyntaksi `cal`-komennolle on seuraava:

```bash
cal [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-m`: Näyttää kuukauden ensimmäisenä päivänä maanantaina.
- `-y`: Näyttää koko vuoden kalenterin.
- `-3`: Näyttää nykyisen kuukauden, edellisen ja seuraavan kuukauden.
- `-j`: Näyttää päivät vuoden päivinä (1-365).

## Yleiset esimerkit
1. **Nykyisen kuukauden kalenteri:**
   ```bash
   cal
   ```

2. **Tietyt kuukausi ja vuosi (esim. joulukuu 2023):**
   ```bash
   cal 12 2023
   ```

3. **Koko vuoden kalenteri (esim. vuosi 2023):**
   ```bash
   cal -y 2023
   ```

4. **Kolme kuukautta kerralla:**
   ```bash
   cal -3
   ```

5. **Kalenteri, jossa päivät näkyvät vuoden päivinä:**
   ```bash
   cal -j
   ```

## Vinkit
- Käytä `cal`-komentoa yhdessä muiden komentojen kanssa, kuten `grep`, suodataksesi tiettyjä päivämääriä.
- Voit yhdistää `cal`-komennon `|`-putkella muihin komentoihin, kuten `less`, jos haluat selata pitkää kalenteria.
- Muista tarkistaa, että käytät oikeaa vuotta ja kuukautta, erityisesti suurissa aikarajoissa, jotta saat tarkat tiedot.