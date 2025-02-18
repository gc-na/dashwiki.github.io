# [Suomi] Debian Almquist Shell (dash) nslookup käyttö: DNS-kyselyiden suorittaminen

## Yleiskatsaus
`nslookup` on työkalu, jota käytetään DNS-kyselyjen suorittamiseen. Sen avulla voit selvittää, mihin IP-osoitteeseen tietty verkkotunnus liittyy tai päinvastoin, mikä verkkotunnus vastaa tiettyä IP-osoitetta.

## Käyttö
Perussyntaksi `nslookup`-komennolle on seuraava:

```bash
nslookup [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-type=tyyppi`: Määrittää kyselyn tyypin, kuten A, AAAA, MX tai CNAME.
- `-timeout=aika`: Asettaa aikarajan kyselyn odottamiselle.
- `-retry=lkm`: Määrittää uusintakyselyjen määrän, jos alkuperäinen kysely epäonnistuu.

## Yleiset esimerkit
1. **Verkkotunnuksen IP-osoitteen selvittäminen:**

```bash
nslookup example.com
```

2. **IP-osoitteen kääntäminen verkkotunnukseksi:**

```bash
nslookup 93.184.216.34
```

3. **MX-tietojen hakeminen:**

```bash
nslookup -type=MX example.com
```

4. **Aikakatkaisun asettaminen kyselylle:**

```bash
nslookup -timeout=5 example.com
```

## Vinkit
- Käytä `-type`-vaihtoehtoa, kun tarvitset erityyppisiä DNS-tietoja.
- Tarkista aina, että käytät oikeaa verkkotunnusta tai IP-osoitetta, jotta saat tarkat tulokset.
- Hyödynnä aikarajoja ja uusintakyselyjä, erityisesti hitaissa verkoissa, jotta voit parantaa kyselyjen luotettavuutta.