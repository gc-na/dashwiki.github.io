# [Suomi] Debian Almquist Shell (dash) rmdir käyttö: Poistaa tyhjät hakemistot

## Yleiskatsaus
`rmdir`-komento on työkalu, jota käytetään tyhjien hakemistojen poistamiseen Unix-pohjaisissa järjestelmissä, kuten Debianissa. Tämä komento ei voi poistaa hakemistoja, jotka sisältävät tiedostoja tai muita hakemistoja.

## Käyttö
Perussyntaksi `rmdir`-komennolle on seuraava:

```bash
rmdir [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-p`: Poistaa myös vanhemmat hakemistot, jos ne ovat tyhjät.
- `--ignore-fail-on-non-empty`: Ohittaa virheen, jos hakemisto ei ole tyhjä.

## Yleiset esimerkit
### Esimerkki 1: Tyhjän hakemiston poistaminen
Jos haluat poistaa tyhjän hakemiston nimeltä `esimerkki`, käytä seuraavaa komentoa:

```bash
rmdir esimerkki
```

### Esimerkki 2: Usean tyhjän hakemiston poistaminen
Voit poistaa useita tyhjiä hakemistoja yhdellä komennolla:

```bash
rmdir hakemisto1 hakemisto2 hakemisto3
```

### Esimerkki 3: Vanhemman hakemiston poistaminen
Jos haluat poistaa tyhjän alihakemiston ja sen vanhemman hakemiston, käytä `-p`-vaihtoehtoa:

```bash
rmdir -p alihakemisto/vanhempi
```

## Vinkit
- Varmista, että hakemisto on tyhjät ennen `rmdir`-komennon käyttöä, muuten komento epäonnistuu.
- Käytä `ls`-komentoa tarkistaaksesi hakemiston sisällön ennen poistamista.
- Ole varovainen `-p`-vaihtoehdon kanssa, sillä se voi poistaa useita hakemistoja kerralla, jos ne ovat tyhjät.