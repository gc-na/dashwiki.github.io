# [Suomi] Debian Almquist Shell (dash) killall käyttö: Prosessien lopettaminen

## Yleiskatsaus
`killall`-komento lopettaa kaikki käynnissä olevat prosessit, joiden nimi vastaa annettua argumenttia. Tämä on hyödyllinen työkalu, kun haluat nopeasti sulkea useita prosesseja yhdellä komennolla.

## Käyttö
Perussyntaksi `killall`-komennolle on seuraava:

```bash
killall [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-u käyttäjä`: Lopettaa vain käyttäjän omistamat prosessit.
- `-i`: Vahvistaa ennen prosessien lopettamista.
- `-q`: Ei tulosta virheilmoituksia, jos prosessia ei löydy.
- `-s signaali`: Määrittää lähetettävän signaalin (oletus on SIGTERM).

## Yleiset esimerkit
1. Kaikkien `firefox`-prosessien lopettaminen:
   ```bash
   killall firefox
   ```

2. Kaikkien `python`-prosessien lopettaminen vahvistusta vaatimatta:
   ```bash
   killall -q python
   ```

3. Kaikkien käyttäjän omistamien `gedit`-prosessien lopettaminen:
   ```bash
   killall -u $USER gedit
   ```

4. Kaikkien `java`-prosessien lopettaminen käyttäen SIGKILL-signaalia:
   ```bash
   killall -s SIGKILL java
   ```

## Vinkit
- Käytä `-i`-vaihtoehtoa, jos et ole varma, mitkä prosessit lopetetaan, jotta voit vahvistaa ennen toiminnan suorittamista.
- Ole varovainen `killall`-komennon kanssa, sillä se voi lopettaa kaikki samannimiset prosessit, mikä voi johtaa tietojen menetykseen tai ohjelmien toimintahäiriöihin.
- Voit tarkistaa, mitkä prosessit ovat käynnissä ennen `killall`-käyttöä komennolla `ps aux | grep [prosessi]`.