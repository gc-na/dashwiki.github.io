# [Suomi] Debian Almquist Shell (dash) fg käyttö: Siirtää taustaprosessin eteen

## Yleiskatsaus
`fg`-komento käytetään siirtämään taustaprosessi aktiiviseksi etuprosessiksi. Tämä on hyödyllistä, kun haluat palata aiemmin keskeytettyyn tai taustalle siirrettyyn prosessiin.

## Käyttö
Perussyntaksi `fg`-komennolle on seuraava:

```bash
fg [valinnat] [argumentit]
```

## Yleiset Valinnat
- `job_spec`: Määrittää, mikä taustaprosessi siirretään eteen. Voit käyttää prosessin numeroa tai nimeä.
- `-n`: Siirtää seuraavan taustaprosessin eteen.
- `-p`: Käyttää prosessin ID:tä (PID) määrittämään, mikä prosessi siirretään.

## Yleiset Esimerkit
Siirretään taustaprosessi eteen:

```bash
fg %1
```

Tässä esimerkissä `%1` viittaa ensimmäiseen taustaprosessiin.

Siirretään seuraava taustaprosessi eteen:

```bash
fg -n
```

Siirretään tietty prosessi käyttäen sen PID:tä:

```bash
fg -p 1234
```

## Vinkit
- Varmista, että tiedät, mitkä prosessit ovat taustalla ennen `fg`-komennon käyttöä. Voit tarkistaa taustaprosessit käyttämällä `jobs`-komentoa.
- Käytä `Ctrl + Z` keskeyttääksesi prosessin ja siirtääksesi sen taustalle ennen `fg`-komennon käyttöä.
- Muista, että `fg`-komento toimii vain niille prosesseille, jotka on käynnistetty nykyisessä istunnossa.