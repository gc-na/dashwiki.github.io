# [Suomi] Debian Almquist Shell (dash) käyttäjät: käyttäjätietojen näyttäminen

## Yleiskatsaus
`users`-komento näyttää tällä hetkellä kirjautuneet käyttäjät järjestelmään. Se listaa käyttäjät, jotka ovat aktiivisesti kirjautuneina, ja voi olla hyödyllinen järjestelmänvalvojille tai käyttäjille, jotka haluavat tarkistaa, ketkä ovat yhteydessä järjestelmään.

## Käyttö
Perussyntaksi `users`-komennolle on seuraava:
```
users [options] [arguments]
```

## Yleiset vaihtoehdot
- `-a`, `--all`: Näyttää kaikki käyttäjät, mukaan lukien ne, jotka ovat kirjautuneet sisään useita kertoja.
- `-r`, `--raw`: Näyttää käyttäjät ilman muotoilua, vain käyttäjänimet.

## Yleiset esimerkit
1. Näytä kaikki tällä hetkellä kirjautuneet käyttäjät:
   ```bash
   users
   ```

2. Näytä kaikki käyttäjät, mukaan lukien useita kirjautumisia:
   ```bash
   users -a
   ```

3. Näytä käyttäjät ilman muotoilua:
   ```bash
   users -r
   ```

## Vinkit
- Käytä `users`-komentoa yhdessä muiden järjestelmänvalvontatyökalujen kanssa, kuten `who` tai `w`, saadaksesi lisätietoja käyttäjistä.
- Voit yhdistää `users`-komennon putkittamalla sen muihin komentoihin, kuten `sort`, järjestääksesi käyttäjälistan aakkosjärjestykseen:
   ```bash
   users | sort
   ```
- Muista, että `users` näyttää vain aktiiviset käyttäjät, joten se ei anna tietoa käyttäjistä, jotka ovat kirjautuneet ulos.