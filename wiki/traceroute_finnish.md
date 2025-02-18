# [Suomi] Debian Almquist Shell (dash) traceroute käyttö: Verkkoreittien jäljittäminen

## Yleiskatsaus
`traceroute`-komento on työkalu, jota käytetään verkkoreittien jäljittämiseen tietokoneen ja kohdeosoitteen välillä. Se näyttää, mitkä reitittimet (tai solmut) paketti kulkee läpi ennen kuin se saavuttaa määränpäänsä. Tämä voi olla hyödyllistä verkko-ongelmien diagnosoinnissa ja suorituskyvyn analysoinnissa.

## Käyttö
Perussyntaksi `traceroute`-komennolle on seuraava:

```bash
traceroute [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-m <max_hops>`: Asettaa maksimi hyppymäärän, jonka traceroute voi tehdä.
- `-p <port>`: Määrittää portin, jota käytetään yhteyden muodostamiseen.
- `-n`: Näyttää IP-osoitteet ilman DNS-nimiä.
- `-w <aika>`: Asettaa aikarajan (sekunteina) odotettavalle vastaukselle.

## Yleiset esimerkit
1. **Perus traceroute**
   ```bash
   traceroute example.com
   ```

2. **Maksimihyppyjen asettaminen**
   ```bash
   traceroute -m 15 example.com
   ```

3. **Portin määrittäminen**
   ```bash
   traceroute -p 80 example.com
   ```

4. **IP-osoitteiden näyttäminen ilman DNS-nimiä**
   ```bash
   traceroute -n example.com
   ```

5. **Aikarajan asettaminen**
   ```bash
   traceroute -w 2 example.com
   ```

## Vinkit
- Käytä `-n`-vaihtoehtoa, jos haluat nopeuttaa komennon suorittamista, erityisesti suurilla verkoilla.
- Tarkista reitittimien vasteajat, jotta voit tunnistaa mahdolliset pullonkaulat verkossa.
- Yhdistä `traceroute` muihin verkko-ongelmien diagnosointityökaluihin, kuten `ping`, saadaksesi kattavamman kuvan verkon tilasta.