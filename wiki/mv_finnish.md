# [Suomi] Debian Almquist Shell (dash) mv käyttö: Tiedostojen siirtäminen ja nimeäminen

## Yleiskatsaus
`mv`-komento on käytettävissä tiedostojen ja hakemistojen siirtämiseen tai nimeämiseen Unix-pohjaisissa käyttöjärjestelmissä, kuten Debianissa. Tämä komento on hyödyllinen, kun haluat järjestää tiedostoja tai muuttaa niiden nimiä.

## Käyttö
Perussyntaksi `mv`-komennolle on seuraava:
```bash
mv [valinnat] [argumentit]
```

## Yleiset valinnat
- `-i`: Kysyy vahvistuksen ennen tiedoston ylikirjoittamista.
- `-u`: Siirtää tiedoston vain, jos lähdetiedosto on uudempi kuin kohdetiedosto tai jos kohdetiedostoa ei ole.
- `-v`: Näyttää siirrettävät tiedostot yksityiskohtaisesti.

## Yleiset esimerkit
Siirretään tiedosto nimeltä `dokumentti.txt` hakemistoon `asiakirjat`:
```bash
mv dokumentti.txt asiakirjat/
```

Nimetään tiedosto `vanha_nimi.txt` uudelleen `uusi_nimi.txt`:
```bash
mv vanha_nimi.txt uusi_nimi.txt
```

Siirretään useita tiedostoja hakemistoon `kuvat`:
```bash
mv kuva1.jpg kuva2.png kuvat/
```

Käytetään `-i`-valintaa, jolloin kysytään vahvistusta ennen ylikirjoittamista:
```bash
mv -i vanha_tiedosto.txt uusi_tiedosto.txt
```

## Vinkit
- Käytä `-v`-valintaa, jos haluat nähdä, mitä tiedostoja siirretään, erityisesti kun siirrät useita tiedostoja kerralla.
- Varmista, että tiedostot, joita yrität siirtää, ovat olemassa, jotta vältät virheilmoituksia.
- Hyödynnä `-u`-valintaa, kun haluat varmistaa, että vain uudemmat tiedostot siirretään, mikä voi säästää aikaa ja vaivannäköä.