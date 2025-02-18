# [Suomi] Debian Almquist Shell (dash) gunzip käyttö: Purkaa gzip-tiedostoja

## Yleiskatsaus
`gunzip`-komento on käytettävissä gzip-pakattujen tiedostojen purkamiseen. Se poistaa gzip-pakkauksen ja palauttaa alkuperäisen tiedoston.

## Käyttö
Perussyntaksi `gunzip`-komennolle on seuraava:

```bash
gunzip [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Tulostaa purkautuneen tiedoston standardiin tulostukseen (stdout) sen sijaan, että se tallennettaisiin tiedostoon.
- `-f`: Pakottaa purkamisen, vaikka tiedosto, johon purku tehdään, on olemassa.
- `-k`: Säilyttää alkuperäisen gzip-tiedoston purkamisen jälkeen.
- `-r`: Purkaa kaikki gzip-tiedostot rekursiivisesti hakemistosta.

## Yleiset esimerkit
1. Yksinkertainen gzip-tiedoston purkaminen:
   ```bash
   gunzip tiedosto.gz
   ```

2. Purkaminen ja alkuperäisen tiedoston säilyttäminen:
   ```bash
   gunzip -k tiedosto.gz
   ```

3. Purkaminen ja tulostaminen standardiin:
   ```bash
   gunzip -c tiedosto.gz > uusi_tiedosto
   ```

4. Rekursiivinen purku hakemistosta:
   ```bash
   gunzip -r hakemisto/
   ```

## Vinkit
- Käytä `-k`-vaihtoehtoa, jos haluat säilyttää alkuperäiset tiedostot purkamisen jälkeen.
- Tarkista purkamisen jälkeen tiedoston koko ja sisältö varmistaaksesi, että se on purkautunut oikein.
- Voit yhdistää `gunzip`-komennon putkiin muiden komentojen kanssa, kuten `tar`, tiedostojen käsittelyä varten.