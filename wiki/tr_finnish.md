# [Suomi] Debian Almquist Shell (dash) tr käyttö: merkkijonojen muuntaminen

## Yleiskatsaus
`tr`-komento on työkalu, jota käytetään merkkijonojen muuntamiseen ja muokkaamiseen. Se voi muuntaa merkkejä, poistaa niitä tai korvata niitä toisilla merkeillä.

## Käyttö
Perussyntaksi `tr`-komennolle on seuraava:
```bash
tr [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d`: Poistaa määritellyt merkit.
- `-s`: Tiivistää peräkkäiset toistuvat merkit yhdeksi.
- `-c`: Käyttää täydentävää merkkiyhdistelmää.
- `-t`: Rajoittaa muunnoksen vain ensimmäisiin merkkeihin.

## Yleiset esimerkit
1. **Merkkien korvaaminen**
   Korvataan kaikki pienet kirjaimet isoilla:
   ```bash
   echo "terve maailma" | tr 'a-z' 'A-Z'
   ```

2. **Merkkien poistaminen**
   Poistetaan kaikki numerot merkkijonosta:
   ```bash
   echo "Terve 123 maailmaa" | tr -d '0-9'
   ```

3. **Peräkkäisten merkkien tiivistäminen**
   Tiivistetään peräkkäiset välilyönnit yhdeksi:
   ```bash
   echo "Terve    maailma" | tr -s ' '
   ```

4. **Merkkiyhdistelmän täydentäminen**
   Korvataan kaikki ei-alfanumeeriset merkit alaviivalla:
   ```bash
   echo "Terve! Maailma?" | tr -c '[:alnum:]' '_'
   ```

## Vinkit
- Käytä `tr`-komentoa yhdessä putkien kanssa, jotta voit käsitellä suuria tietomääriä tehokkaasti.
- Muista, että `tr` ei muokkaa tiedostoja suoraan, vaan se toimii syötteen ja tulosteen välillä.
- Testaa komento ensin pienillä merkkijonoilla varmistaaksesi, että se toimii odotetusti ennen kuin käytät sitä suuremmissa tiedostoissa.