# [Suomi] Debian Almquist Shell (dash) whoami käyttö: Näyttää nykyisen käyttäjän nimen

## Yleiskatsaus
`whoami`-komento näyttää sen käyttäjän nimen, joka tällä hetkellä on kirjautuneena järjestelmään. Tämä komento on hyödyllinen, kun halutaan varmistaa, että käytetään oikeaa käyttäjätiliä, erityisesti monikäyttäjäjärjestelmissä.

## Käyttö
Perussyntaksi `whoami`-komennolle on seuraava:

```bash
whoami [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- **--help**: Näyttää apuviestin ja käytön ohjeet.
- **--version**: Näyttää ohjelman versionumeron.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `whoami`-komennon käytöstä:

1. **Nykyisen käyttäjän nimen näyttäminen**:
   ```bash
   whoami
   ```

2. **Apuviestin näyttäminen**:
   ```bash
   whoami --help
   ```

3. **Version tarkistaminen**:
   ```bash
   whoami --version
   ```

## Vinkit
- Käytä `whoami`-komentoa varmistaaksesi, että olet oikeassa käyttäjätilissä ennen kriittisten toimintojen suorittamista.
- Voit yhdistää `whoami`-komennon muihin komentoihin, kuten `echo`, saadaksesi selkeämmän tulosteen:
  ```bash
  echo "Olet kirjautuneena käyttäjänä: $(whoami)"
  ```
- Muista, että `whoami` palauttaa vain käyttäjän nimen, ei muita tietoja tai käyttöoikeuksia.