# [Suomi] Debian Almquist Shell (dash) renice käyttö: Prosessien prioriteetin muuttaminen

## Overview
`renice`-komento käytetään prosessien prioriteettitason muuttamiseen Linux-järjestelmässä. Sen avulla voit nostaa tai laskea prosessin prioriteettiä, mikä vaikuttaa siihen, kuinka paljon CPU-aikaa prosessi saa verrattuna muihin prosesseihin.

## Usage
Perussyntaksi `renice`-komennolle on seuraava:

```bash
renice [options] [arguments]
```

## Common Options
- `-n, --priority <number>`: Määrittää uuden prioriteettitason. Arvo voi olla -20 (korkein prioriteetti) ja 19 (alin prioriteetti).
- `-p, --pid <pid>`: Muuttaa tietyn prosessin prioriteettia, jossa `<pid>` on prosessin tunnus.
- `-g, --pgrp <pgrp>`: Muuttaa prosessiryhmän prioriteettia.
- `-u, --user <user>`: Muuttaa tietyn käyttäjän kaikkien prosessien prioriteettia.

## Common Examples
1. Muuta prosessin prioriteettia prosessin tunnuksen mukaan:
   ```bash
   renice -n 10 -p 1234
   ```
   Tämä asettaa prosessin, jonka tunnus on 1234, prioriteetiksi 10.

2. Muuta kaikkien tietyn käyttäjän prosessien prioriteettia:
   ```bash
   renice -n 5 -u käyttäjä
   ```
   Tämä asettaa kaikkien käyttäjän "käyttäjä" prosessien prioriteetiksi 5.

3. Muuta prosessiryhmän prioriteettia:
   ```bash
   renice -n -5 -g 5678
   ```
   Tämä asettaa prosessiryhmän, jonka tunnus on 5678, prioriteetiksi -5.

## Tips
- Käytä `renice`-komentoa varoen, sillä liian korkea prioriteetti voi aiheuttaa järjestelmän hidastumista.
- Tarkista prosessien nykyiset prioriteetit ennen muutoksia komennolla `ps -o pid,pri,cmd`.
- Varmista, että sinulla on tarvittavat oikeudet muuttaa muiden käyttäjien prosessien prioriteetteja, yleensä vaaditaan superkäyttäjän oikeudet.