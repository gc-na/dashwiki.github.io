# [Suomi] Debian Almquist Shell (dash) chown: [omistajuuden muuttaminen]

## Overview
`chown`-komento (change owner) muuttaa tiedostojen tai hakemistojen omistajuutta Unix-pohjaisissa järjestelmissä. Voit määrittää uuden omistajan ja tarvittaessa myös ryhmän.

## Usage
Perussyntaksi `chown`-komennolle on seuraava:

```bash
chown [options] [new_owner][:new_group] [file...]
```

## Common Options
- `-R`: Muuttaa omistajuuden rekursiivisesti hakemistossa ja sen alihakemistoissa.
- `-v`: Näyttää yksityiskohtaisen tulosteen jokaisesta muutoksesta.
- `--reference=FILE`: Asettaa omistajuuden viitatun tiedoston omistajuuden mukaan.

## Common Examples
- Muuta tiedoston `example.txt` omistajaksi käyttäjä `user1`:

```bash
chown user1 example.txt
```

- Muuta hakemiston `myfolder` omistajaksi käyttäjä `user2` rekursiivisesti:

```bash
chown -R user2 myfolder
```

- Muuta tiedoston `example.txt` omistajaksi käyttäjä `user1` ja ryhmäksi `group1`:

```bash
chown user1:group1 example.txt
```

- Muuta usean tiedoston omistajaksi käyttäjä `user3`:

```bash
chown user3 file1.txt file2.txt file3.txt
```

## Tips
- Varmista, että sinulla on tarvittavat oikeudet muuttaa tiedostojen omistajuutta.
- Käytä `-v`-optiota, jotta näet, mitä muutoksia teet, erityisesti suurissa hakemistoissa.
- Ole varovainen käyttäessäsi `-R`-optiota, sillä se voi muuttaa omistajuuden kaikille tiedostoille ja hakemistoille rekursiivisesti.