# [Suomi] Debian Almquist Shell (dash) bg käyttö: Taustaprosessien aktivointi

## Yleiskatsaus
`bg`-komento käytetään taustaprosessien aktivointiin, jolloin käyttäjä voi jatkaa työskentelyä komentorivillä, vaikka prosessi suoritetaan taustalla.

## Käyttö
Perussyntaksi komennolle on seuraava:
```bash
bg [options] [arguments]
```

## Yleiset vaihtoehdot
- `job_id`: Määrittelee taustaprosessin, joka halutaan aktivoida. Voit käyttää joko prosessin numeroa tai sen nimeä.
- `-l`: Näyttää kaikki taustaprosessit, jotka ovat käynnissä.

## Yleiset esimerkit
1. **Taustaprosessin aktivointi**:
   Jos olet käynnistänyt prosessin, kuten `sleep 60`, ja keskeyttänyt sen (esimerkiksi painamalla `Ctrl+Z`), voit aktivoida sen taustalle seuraavasti:
   ```bash
   bg %1
   ```
   Tässä `%1` viittaa ensimmäiseen keskeytettyyn prosessiin.

2. **Kaikkien taustaprosessien listaaminen**:
   Voit tarkistaa kaikki taustaprosessit komennolla:
   ```bash
   jobs
   ```

3. **Taustaprosessin aktivointi ilman job_id:tä**:
   Jos sinulla on vain yksi keskeytetty prosessi, voit yksinkertaisesti käyttää:
   ```bash
   bg
   ```

## Vinkit
- Muista tarkistaa aktiiviset prosessit `jobs`-komennolla ennen `bg`-komennon käyttöä.
- Voit käyttää `fg`-komentoa palauttaaksesi prosessin etualalle, jos tarvitset sen vuorovaikutteista käyttöä.
- Käytä `nohup`-komentoa yhdessä `bg`:n kanssa, jos haluat varmistaa, että prosessi jatkaa toimintaansa myös kirjautuessasi ulos.