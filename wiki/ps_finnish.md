# [Suomi] Debian Almquist Shell (dash) ps käyttö: [näyttää prosessit]

## Yleiskatsaus
`ps`-komento on työkalu, jota käytetään prosessien näyttämiseen ja hallintaan Unix-tyyppisissä käyttöjärjestelmissä, kuten Debianissa. Se tarjoaa tietoa käynnissä olevista prosesseista, mukaan lukien niiden prosessitunnukset (PID), tila ja resurssinkäyttö.

## Käyttö
Perussyntaksi `ps`-komennolle on seuraava:

```bash
ps [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e` tai `-A`: Näyttää kaikki prosessit.
- `-f`: Näyttää prosessit täydellisessä muodossa, mukaan lukien vanhempi-prosessitiedot.
- `-u [käyttäjä]`: Näyttää vain tietyn käyttäjän prosessit.
- `-aux`: Näyttää kaikki prosessit laajennetussa muodossa.
- `--sort=[kenttä]`: Järjestää tulokset tietyn kentän mukaan, kuten `pid` tai `cpu`.

## Yleiset esimerkit
1. Kaikkien prosessien näyttäminen:
   ```bash
   ps -e
   ```

2. Prosessien näyttäminen täydellisessä muodossa:
   ```bash
   ps -f
   ```

3. Tietyn käyttäjän prosessien näyttäminen:
   ```bash
   ps -u käyttäjänimi
   ```

4. Kaikkien prosessien näyttäminen laajennetussa muodossa:
   ```bash
   ps aux
   ```

5. Prosessien järjestäminen CPU-käytön mukaan:
   ```bash
   ps --sort=-%cpu
   ```

## Vinkit
- Käytä `ps aux` -komentoa saadaksesi kattavan näkymän kaikista prosesseista, mukaan lukien niiden resurssinkäyttö.
- Yhdistä `ps`-komento muihin komentoriviohjelmiin, kuten `grep`, suodataksesi tuloksia. Esimerkiksi:
  ```bash
  ps aux | grep ohjelman_nimi
  ```
- Muista, että `ps` näyttää vain ne prosessit, joilla on käyttöoikeus käyttäjätilillesi, ellei käytä `sudo`-komentoa.