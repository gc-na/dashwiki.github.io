# [Suomi] Debian Almquist Shell (dash) mtr käyttö: Verkkoyhteyksien diagnosointi

## Yleiskatsaus
mtr (My Traceroute) on työkalu, joka yhdistää traceroute- ja ping-komentojen toiminnot. Se näyttää reitin, jota pitkin paketit kulkevat kohdeosoitteeseen, sekä mittaa viiveitä ja pakettihäviöitä jokaisessa väliportissa. Tämä tekee siitä erinomaisen työkalun verkkoyhteyksien diagnosointiin.

## Käyttö
Perussyntaksi mtr-komennolle on seuraava:

```bash
mtr [vaihtoehdot] [osoite]
```

## Yhteiset vaihtoehdot
- `-r`: Suorita mtr "raportti"-tilassa, joka näyttää yhteenvedon.
- `-c [luku]`: Määritä, kuinka monta pakettia lähetetään (esim. `-c 10`).
- `-n`: Älä tee DNS-nimeämistä, vaan näytä vain IP-osoitteet.
- `-i [aika]`: Määritä aikaväli pakettien lähettämiseen sekunneissa (esim. `-i 0.5`).

## Yhteiset esimerkit
1. Perus mtr-komento kohdeosoitteelle:
   ```bash
   mtr example.com
   ```

2. Raporttimuodossa, jossa lähetetään 10 pakettia:
   ```bash
   mtr -r -c 10 example.com
   ```

3. IP-osoitteiden näyttäminen ilman DNS-nimeämistä:
   ```bash
   mtr -n example.com
   ```

4. Pakettien lähettämisen aikavälin määrittäminen:
   ```bash
   mtr -i 0.5 example.com
   ```

## Vinkit
- Käytä `-r`-vaihtoehtoa, kun haluat saada yhteenvedon yhteydestäsi, erityisesti ongelmatilanteissa.
- Jos haluat tarkastella reittiä ilman DNS-nimeämistä, käytä `-n`-vaihtoehtoa, mikä voi nopeuttaa tulosten saamista.
- Muista, että mtr voi vaatia root-oikeuksia tietyissä ympäristöissä, joten käytä `sudo`-komentoa tarvittaessa.