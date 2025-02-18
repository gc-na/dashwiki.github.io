# [Suomi] Debian Almquist Shell (dash) umask käyttö: Tiedostojen oletusoikeuksien määrittäminen

## Yleiskatsaus
`umask`-komento määrittää oletusoikeudet uusille tiedostoille ja hakemistoille, jotka luodaan käyttäjän toimesta. Se määrittää, mitkä oikeudet poistetaan tiedostojen ja hakemistojen oletusoikeuksista.

## Käyttö
Perussyntaksi `umask`-komennolle on seuraava:

```bash
umask [options] [arguments]
```

## Yleiset vaihtoehdot
- `-S`: Näyttää umaskin nykyiset oikeudet symbolisessa muodossa.
- `-p`: Tulostaa nykyisen umaskin arvon, mutta ei muuta sitä.

## Yleiset esimerkit
### 1. Nykyisen umaskin tarkistaminen
Voit tarkistaa nykyisen umask-arvon suorittamalla seuraavan komennon:

```bash
umask
```

### 2. Umaskin asettaminen
Voit asettaa umask-arvoksi esimerkiksi `022`, jolloin uusien tiedostojen oletusoikeudet ovat `rw-r--r--` ja hakemistojen `rwxr-xr-x`:

```bash
umask 022
```

### 3. Umaskin näyttäminen symbolisessa muodossa
Jos haluat nähdä umaskin nykyiset oikeudet symbolisessa muodossa, käytä seuraavaa komentoa:

```bash
umask -S
```

### 4. Umaskin palauttaminen oletusarvoon
Jos haluat palauttaa umaskin oletusarvoon, voit asettaa sen esimerkiksi `002`:

```bash
umask 002
```

## Vinkit
- Muista, että umask-arvo vaikuttaa vain uusiin tiedostoihin ja hakemistoihin, ei olemassa oleviin.
- Hyvä käytäntö on tarkistaa umask-arvo ennen tärkeiden tiedostojen luomista, jotta oikeudet ovat haluamasi mukaiset.
- Voit lisätä umask-asetuksen käyttäjän shellin konfiguraatiotiedostoon (esim. `.profile` tai `.bashrc`), jotta se asetetaan automaattisesti kirjautuessasi sisään.