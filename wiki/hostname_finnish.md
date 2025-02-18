# [Suomi] Debian Almquist Shell (dash) hostname käyttö: [näyttää tai asettaa isäntänimen]

## Yleiskatsaus
`hostname`-komento käytetään isäntänimen näyttämiseen tai asettamiseen Unix-pohjaisissa järjestelmissä. Isäntänimi on tietokoneen verkko-osoite, jota käytetään sen tunnistamiseen verkossa.

## Käyttö
Perussyntaksi komennolle on seuraava:
```bash
hostname [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`, `--fqdn`: Näyttää täydellisen isäntänimen (Fully Qualified Domain Name).
- `-i`, `--ip-address`: Näyttää isäntänimen IP-osoitteen.
- `-s`, `--short`: Näyttää lyhyen isäntänimen.
- `--help`: Näyttää apuviestin komennosta.
- `--version`: Näyttää versionumeron.

## Yleiset esimerkit
1. **Isäntänimen näyttäminen**
   ```bash
   hostname
   ```

2. **Täydellisen isäntänimen näyttäminen**
   ```bash
   hostname -f
   ```

3. **Isäntänimen IP-osoitteen näyttäminen**
   ```bash
   hostname -i
   ```

4. **Lyhyen isäntänimen näyttäminen**
   ```bash
   hostname -s
   ```

5. **Isäntänimen asettaminen**
   ```bash
   sudo hostname uusi_isäntänimi
   ```

## Vinkit
- Muista, että isäntänimen muuttaminen vaatii usein pääkäyttäjän oikeudet, joten käytä `sudo`-komentoa.
- Isäntänimen muutokset eivät välttämättä vaikuta heti, joten saatat joutua käynnistämään järjestelmän uudelleen tai päivittämään verkkoyhteydet.
- Tarkista isäntänimen muutoksen jälkeen, että se on oikein asetettu käyttämällä `hostname`-komentoa uudelleen.