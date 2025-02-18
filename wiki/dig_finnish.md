# [Suomi] Debian Almquist Shell (dash) dig käyttö: DNS-tietojen hakeminen

## Yleiskatsaus
`dig` (Domain Information Groper) on työkalu, jota käytetään DNS-tietojen hakemiseen ja tutkimiseen. Se mahdollistaa käyttäjille DNS-kyselyjen tekemisen ja tulosten tarkastelun, mikä on hyödyllistä verkkotunnusten ja IP-osoitteiden selvittämisessä.

## Käyttö
Perussyntaksi `dig`-komennolle on seuraava:

```bash
dig [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `@server`: Määrittää DNS-palvelimen, jolta kysely tehdään.
- `-t type`: Määrittää kyselyn tyypin, kuten A, AAAA, MX, CNAME jne.
- `+short`: Näyttää vain lyhyen vastauksen, joka on helpompi lukea.
- `+trace`: Seuraa kyselyn reittiä DNS-palvelimien läpi.

## Yleiset esimerkit
### 1. Peruskysely
Hae verkkotunnuksen IP-osoite:
```bash
dig example.com
```

### 2. Tietyn tyyppinen kysely
Hae verkkotunnuksen MX-tietueet:
```bash
dig -t MX example.com
```

### 3. Kysely tietyltä DNS-palvelimelta
Kysy tietoja Google DNS:ltä:
```bash
dig @8.8.8.8 example.com
```

### 4. Lyhyt vastaus
Hae verkkotunnuksen IP-osoite lyhyessä muodossa:
```bash
dig +short example.com
```

### 5. Kyselyn jäljittäminen
Seuraa kyselyä DNS-palvelimien läpi:
```bash
dig +trace example.com
```

## Vinkit
- Käytä `+short`-vaihtoehtoa, kun haluat nopean ja selkeän vastauksen.
- Hyödynnä `-t`-vaihtoehtoa, kun tarvitset erityisiä tietueita, kuten MX tai CNAME.
- Kokeile `+trace`-vaihtoehtoa ongelmien selvittämisessä, jolloin näet, miten kysely etenee eri palvelimien kautta.