# [Suomi] Debian Almquist Shell (dash) traceroute6 käyttö: Verkkoreittien jäljittäminen IPv6:lle

## Overview
`traceroute6` on työkalu, joka jäljittää verkkoreittejä IPv6-protokollan kautta. Se näyttää, miten paketit kulkevat verkossa tietokoneelta toiseen, mikä auttaa diagnosoimaan verkko-ongelmia ja ymmärtämään verkkoyhteyksien rakennetta.

## Usage
Perussyntaksi `traceroute6`-komennolle on seuraava:

```bash
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: Määrittää suurimman Time-To-Live (TTL) arvon.
- `-n`: Näyttää IP-osoitteet ilman DNS-nimiä.
- `-p <port>`: Määrittää portin, jota käytetään UDP-paketeissa.
- `-q <nqueries>`: Määrittää kyselyjen määrän jokaiselle reitittimelle.

## Common Examples
1. **Perusreitin jäljittäminen**
   ```bash
   traceroute6 google.com
   ```

2. **Reitin jäljittäminen tiettyyn porttiin**
   ```bash
   traceroute6 -p 80 google.com
   ```

3. **Reitin jäljittäminen ilman DNS-nimiä**
   ```bash
   traceroute6 -n google.com
   ```

4. **Maksim TTL:n määrittäminen**
   ```bash
   traceroute6 -m 30 google.com
   ```

## Tips
- Käytä `-n`-optiota, jos haluat nopeuttaa komennon suoritusta, koska DNS-kyselyt voivat hidastaa prosessia.
- Tarkista, että IPv6-yhteys on toiminnassa ennen `traceroute6`-komennon suorittamista.
- Hyödynnä `-m`-optiota, jos haluat rajoittaa jäljityksen syvyyttä ja välttää ylimääräisiä reitittimiä.