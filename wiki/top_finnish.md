# [Suomi] Debian Almquist Shell (dash) top käyttö: prosessien seuranta

## Yleiskatsaus
`top`-komento on työkalu, joka näyttää reaaliaikaisesti järjestelmän prosessit ja niiden resurssinkäytön. Se tarjoaa käyttäjälle mahdollisuuden seurata, mitkä prosessit kuluttavat eniten CPU:a ja muistia, sekä muita tärkeitä tietoja järjestelmän tilasta.

## Käyttö
Perussyntaksi `top`-komennolle on seuraava:

```bash
top [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-d <aika>`: Määrittää päivitysvälin sekunneissa.
- `-n <kerrat>`: Määrittää, kuinka monta kertaa `top`-näyttö päivitetään ennen lopettamista.
- `-u <käyttäjä>`: Näyttää vain tietyn käyttäjän prosessit.

## Yleiset esimerkit
- **Peruskomento**: Käynnistää `top`-näytön.
  ```bash
  top
  ```

- **Päivitysvälin asettaminen**: Aseta päivitysväliksi 5 sekuntia.
  ```bash
  top -d 5
  ```

- **Rajoita käyttäjän prosessit**: Näytä vain käyttäjän "user1" prosessit.
  ```bash
  top -u user1
  ```

- **Rajoita päivityksiä**: Näytä prosessit 10 kertaa ja lopeta sitten.
  ```bash
  top -n 10
  ```

## Vinkit
- Voit käyttää näppäimistön komentoja `top`-tilassa, kuten `M` järjestääksesi prosessit muistin käytön mukaan tai `P` järjestääksesi ne CPU:n käytön mukaan.
- Hyödynnä `k`-komentoa tappamaan prosesseja suoraan `top`-näkymästä syöttämällä prosessin ID.
- Muista, että `top`-komento voi näyttää suuren määrän tietoa, joten käytä suodatusvaihtoehtoja tehokkaasti, jotta saat tarvitsemasi tiedot nopeasti.