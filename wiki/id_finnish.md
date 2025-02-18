# [Suomi] Debian Almquist Shell (dash) id käyttö: käyttäjän tunnistaminen

## Yleiskatsaus
`id`-komento näyttää käyttäjän tunnistetiedot, kuten käyttäjänimen, käyttäjä-ID:n (UID), ryhmä-ID:n (GID) ja käyttäjän liittymät ryhmät. Tämä komento on hyödyllinen, kun halutaan tarkistaa, mihin käyttäjäryhmiin käyttäjä kuuluu tai saada tietoa käyttäjän oikeuksista.

## Käyttö
Perussyntaksi `id`-komennolle on seuraava:
```bash
id [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-u`: Näyttää vain käyttäjä-ID:n (UID).
- `-g`: Näyttää vain ryhmä-ID:n (GID).
- `-G`: Näyttää kaikki käyttäjän ryhmä-ID:t.
- `-n`: Näyttää käyttäjän tai ryhmän nimen sen sijaan, että näyttäisi ID:n.

## Yleiset esimerkit
1. Näytä nykyisen käyttäjän tiedot:
   ```bash
   id
   ```

2. Näytä vain käyttäjä-ID:
   ```bash
   id -u
   ```

3. Näytä vain ryhmä-ID:
   ```bash
   id -g
   ```

4. Näytä kaikki ryhmä-ID:t:
   ```bash
   id -G
   ```

5. Näytä toisen käyttäjän tiedot (esim. käyttäjä "kalle"):
   ```bash
   id kalle
   ```

## Vinkit
- Käytä `id`-komentoa yhdessä muiden komentojen kanssa, kuten `grep`, suodataksesi tietoja.
- Muista, että `id`-komento voi vaatia oikeuksia, jos yrität tarkistaa muiden käyttäjien tietoja.
- Käytä `man id` saadaksesi lisätietoja ja vaihtoehtoja komennosta.