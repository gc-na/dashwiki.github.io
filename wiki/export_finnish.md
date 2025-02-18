# [Suomi] Debian Almquist Shell (dash) export käyttö: ympäristömuuttujien asettaminen

## Yleiskatsaus
`export`-komento käytetään ympäristömuuttujien asettamiseen ja jakamiseen alikomennoille. Kun muuttuja on viety, se on käytettävissä kaikissa sen jälkeen käynnistetyissä prosesseissa.

## Käyttö
Perussyntaksi `export`-komennolle on seuraava:

```sh
export [options] [arguments]
```

## Yleiset vaihtoehdot
- `-p`: Näyttää kaikki vietyjä ympäristömuuttujia.
- `VAR=value`: Asettaa ympäristömuuttujan `VAR` arvoksi `value` ja vie sen.

## Yleiset esimerkit

### Ympäristömuuttujan asettaminen
Voit asettaa ja viedä ympäristömuuttujan seuraavasti:

```sh
export MY_VAR="Hello, World!"
```

### Ympäristömuuttujan tarkistaminen
Voit tarkistaa, että muuttuja on asetettu oikein käyttämällä `echo`-komentoa:

```sh
echo $MY_VAR
```

### Useiden muuttujien vienti
Voit viedä useita muuttujia yhdellä komennolla:

```sh
export VAR1="Value1" VAR2="Value2"
```

### Vietyjen muuttujien näyttäminen
Voit näyttää kaikki vietyjä ympäristömuuttujia komennolla:

```sh
export -p
```

## Vinkit
- Muista, että `export`-komento vie vain senhetkiset muuttujat, joten varmista, että asetat ne ennen alikomentojen suorittamista.
- Käytä `unset`-komentoa poistaaksesi ympäristömuuttujan käytöstä, jos sitä ei enää tarvita.
- Ympäristömuuttujat ovat herkkiä isoille ja pienille kirjaimille, joten varmista, että käytät oikeaa kirjoitusasua.