# [Suomi] Debian Almquist Shell (dash) w: [näyttää käyttäjätiedot]

## Overview
`w`-komento näyttää tietoja järjestelmän käyttäjistä, jotka ovat tällä hetkellä kirjautuneina. Se tarjoaa tietoa käyttäjien aktiivisuudesta, kuten heidän kirjautumisaikansa, käytössä oleva terminaali ja käynnissä olevat prosessit.

## Usage
Perussyntaksi `w`-komennolle on seuraava:
```
w [options] [arguments]
```

## Common Options
- `-h`: Poistaa otsikkorivin tulosteesta.
- `-s`: Näyttää lyhyemmän version tulosteesta, jossa on vain tärkeimmät tiedot.
- `-u`: Näyttää käyttäjän viimeisen inaktiivisuuden ajan.

## Common Examples
### Esimerkki 1: Perustuloste
Tulosta kaikki kirjautuneet käyttäjät ja heidän aktiivisuutensa:
```bash
w
```

### Esimerkki 2: Lyhyt tuloste
Tulosta käyttäjätiedot lyhyessä muodossa:
```bash
w -s
```

### Esimerkki 3: Otsikon poistaminen
Tulosta käyttäjätiedot ilman otsikkoriviä:
```bash
w -h
```

### Esimerkki 4: Inaktiivisuuden näyttäminen
Tulosta käyttäjätiedot ja näytä inaktiivisuuden aika:
```bash
w -u
```

## Tips
- Käytä `w`-komentoa yhdessä muiden järjestelmänvalvontatyökalujen kanssa, kuten `top` tai `htop`, saadaksesi kattavamman kuvan järjestelmän käytöstä.
- Voit yhdistää `w`-komennon putkittamiseen muihin komentoihin, kuten `grep`, suodattaaksesi tuloksia tiettyjen käyttäjien tai prosessien mukaan.