# [Suomi] Debian Almquist Shell (dash) touch käyttö: Tiedostojen aikaleimojen päivittäminen

## Yleiskatsaus
`touch`-komento on yksinkertainen työkalu, jota käytetään tiedostojen aikaleimojen päivittämiseen tai uusien tyhjien tiedostojen luomiseen. Jos tiedosto ei ole olemassa, `touch` luo sen tyhjänä.

## Käyttö
Perussyntaksi `touch`-komennolle on seuraava:

```bash
touch [options] [arguments]
```

## Yleiset vaihtoehdot
- `-a`: Päivittää vain viimeksi käytetyn aikaleiman.
- `-m`: Päivittää vain viimeksi muokattua aikaleimaa.
- `-c`: Ei luo uutta tiedostoa, jos se ei ole olemassa.
- `-t`: Määrittää aikaleiman tietyssä muodossa (YYYYMMDDhhmm).

## Yleiset esimerkit
1. **Uuden tyhjän tiedoston luominen:**
   ```bash
   touch uusi_tiedosto.txt
   ```

2. **Tiedoston aikaleiman päivittäminen:**
   ```bash
   touch olemassa_oleva_tiedosto.txt
   ```

3. **Vain viimeksi käytetyn aikaleiman päivittäminen:**
   ```bash
   touch -a olemassa_oleva_tiedosto.txt
   ```

4. **Vain viimeksi muokattua aikaleimaa päivittäminen:**
   ```bash
   touch -m olemassa_oleva_tiedosto.txt
   ```

5. **Aikaleiman määrittäminen tietyssä muodossa:**
   ```bash
   touch -t 202310011230 uusi_tiedosto.txt
   ```

## Vinkit
- Käytä `-c`-vaihtoehtoa, jos et halua luoda uutta tiedostoa vahingossa.
- Voit käyttää `touch`-komentoa useiden tiedostojen päivittämiseen kerralla erottamalla tiedostonimet välilyönneillä.
- Tarkista tiedostojen aikaleimat komennolla `ls -l` varmistaaksesi, että `touch` on toiminut oikein.