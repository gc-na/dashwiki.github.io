# [Suomi] Debian Almquist Shell (dash) nohup käyttö: Estää prosessin lopettamisen kirjautumisen ulkopuolella

## Yleiskatsaus
`nohup` (no hang up) on komento, joka estää prosessia lopettamasta, kun käyttäjä kirjautuu ulos järjestelmästä. Tämä on erityisen hyödyllistä pitkäkestoisissa tehtävissä, jotka halutaan pitää käynnissä vaikka käyttäjä sulkee istunnon.

## Käyttö
Perussyntaksi `nohup`-komennolle on seuraava:

```
nohup [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `&`: Suorittaa komennon taustalla.
- `-h`: Näyttää apua ja käytön ohjeet.
- `-p`: Käynnistää prosessin ja liittää sen tiettyyn prosessitunnukseen.

## Yleiset esimerkit
1. Suorita pitkäkestoinen skripti taustalla:
   ```bash
   nohup ./pitkä_skripti.sh &
   ```

2. Tallenna komennon tuloste tiedostoon:
   ```bash
   nohup python3 ohjelma.py > tuloste.txt &
   ```

3. Käynnistä komento, joka ei lopeta kirjautumisen yhteydessä:
   ```bash
   nohup komento &
   ```

## Vinkit
- Käytä `&`-merkkiä, jotta komento suoritetaan taustalla, jolloin voit jatkaa muiden komentojen käyttöä.
- Tarkista `nohup.out`-tiedosto, jos et ole määrittänyt tulostetta toiseen tiedostoon; se sisältää komennon tulosteen.
- Varmista, että komento on oikein määritetty ennen `nohup`-käyttöä, jotta vältät virheitä pitkissä suorituksissa.