# [Suomi] Debian Almquist Shell (dash) mkdir käyttö: Luo hakemistoja

## Yleiskatsaus
`mkdir`-komento (make directory) käytetään hakemistojen luomiseen Unix-pohjaisissa käyttöjärjestelmissä, kuten Debianissa. Sen avulla voit luoda uusia hakemistoja tiedostojärjestelmään.

## Käyttö
Perussyntaksi `mkdir`-komennolle on seuraava:

```bash
mkdir [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-p`: Luo tarvittaessa vanhemmat hakemistot.
- `-v`: Näyttää viestin jokaisesta luodusta hakemistosta.
- `--mode=MODE`: Asettaa luodun hakemiston käyttöoikeudet.

## Yleiset esimerkit
### Yksinkertainen hakemiston luominen
Luo hakemisto nimeltä "uusi_hakemisto":
```bash
mkdir uusi_hakemisto
```

### Useiden hakemistojen luominen
Luo useita hakemistoja kerralla:
```bash
mkdir hakemisto1 hakemisto2 hakemisto3
```

### Vanhempien hakemistojen luominen
Luo hakemisto ja sen vanhemmat tarvittaessa:
```bash
mkdir -p vanhempi_hakemisto/uusi_hakemisto
```

### Näyttää luodut hakemistot
Käytä `-v`-vaihtoehtoa nähdäksesi luodut hakemistot:
```bash
mkdir -v uusi_hakemisto
```

## Vinkit
- Käytä `-p`-vaihtoehtoa, kun et ole varma, onko vanhempia hakemistoja olemassa.
- Tarkista käyttöoikeudet luodessasi hakemistoja, erityisesti palvelimilla, joissa on tiukat käyttöoikeudet.
- Voit käyttää `mkdir`-komentoa skripteissä automaattisesti hakemistojen luomiseksi, mikä helpottaa työskentelyä suurissa projekteissa.