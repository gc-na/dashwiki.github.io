# [Suomi] Debian Almquist Shell (dash) pkill käyttö: Prosessien lopettaminen nimen mukaan

## Yleiskatsaus
`pkill`-komento on työkalu, jota käytetään prosessien lopettamiseen niiden nimen perusteella. Se on hyödyllinen, kun haluat sulkea useita prosesseja kerralla ilman, että sinun tarvitsee etsiä niiden prosessitunnuksia (PID).

## Käyttö
Perussyntaksi `pkill`-komennolle on seuraava:

```bash
pkill [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`: Etsii prosessien nimiä täydellisinä komentoina.
- `-n`: Lopettaa vain uusimman prosessin, joka vastaa hakuehtoja.
- `-o`: Lopettaa vain vanhimman prosessin, joka vastaa hakuehtoja.
- `-signal`: Määrittää lähetettävän signaalin (oletus on TERM).

## Yleiset esimerkit
1. Kaikkien `firefox`-prosessejen lopettaminen:
   ```bash
   pkill firefox
   ```

2. Kaikkien `python`-prosessejen lopettaminen, mukaan lukien täydellinen komento:
   ```bash
   pkill -f python
   ```

3. Vain uusimman `ssh`-prosessin lopettaminen:
   ```bash
   pkill -n ssh
   ```

4. Tietyn signaalin lähettäminen `myapp`-prosesseille:
   ```bash
   pkill -SIGKILL myapp
   ```

## Vinkit
- Käytä `-f`-vaihtoehtoa, jos prosessin nimi ei ole yksiselitteinen ja haluat varmistaa, että suljet oikean prosessin.
- Ole varovainen, kun käytät `pkill`-komentoa, sillä se voi lopettaa useita prosesseja kerralla, mikä voi vaikuttaa järjestelmän toimintaan.
- Voit testata komennon toimivuutta käyttämällä `-l`-vaihtoehtoa, joka listaa kaikki prosessit, jotka vastaavat hakuehtojasi ennen niiden lopettamista.