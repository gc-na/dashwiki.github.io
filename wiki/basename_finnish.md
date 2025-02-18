# [Suomi] Debian Almquist Shell (dash) basename käyttö: [tiedostonimen erottaminen polusta]

## Yleiskatsaus
`basename`-komento on työkalu, jota käytetään tiedostopolkujen käsittelyyn. Se poistaa polun osat ja palauttaa vain tiedoston nimen. Tämä on hyödyllistä, kun halutaan käsitellä vain tiedostonimeä ilman sen sijaintia.

## Käyttö
Perussyntaksi `basename`-komennolle on seuraava:

```bash
basename [options] [arguments]
```

## Yleiset vaihtoehdot
- `-a`: Käsittele useita argumentteja ja palauta jokaisen tiedoston nimen.
- `-s`: Poista määritetty loppuliite tiedoston nimestä.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `basename`-komennon käytöstä:

1. **Perustiedoston nimen saaminen polusta:**
   ```bash
   basename /home/kayttaja/tiedostot/tiedosto.txt
   ```
   Tämä palauttaa:
   ```
   tiedosto.txt
   ```

2. **Useiden tiedostojen nimien saaminen:**
   ```bash
   basename -a /home/kayttaja/tiedostot/tiedosto1.txt /home/kayttaja/tiedostot/tiedosto2.txt
   ```
   Tämä palauttaa:
   ```
   tiedosto1.txt
   tiedosto2.txt
   ```

3. **Loppuliitteen poistaminen tiedoston nimestä:**
   ```bash
   basename /home/kayttaja/tiedostot/tiedosto.txt .txt
   ```
   Tämä palauttaa:
   ```
   tiedosto
   ```

## Vinkit
- Käytä `-a`-vaihtoehtoa, kun haluat käsitellä useita tiedostoja kerralla.
- Muista, että `basename` ei muokkaa alkuperäistä tiedostoa, vaan palauttaa vain sen nimen.
- Yhdistä `basename` muihin komentoihin, kuten `find`, saadaksesi tehokkaampia tuloksia tiedostojen käsittelyssä.