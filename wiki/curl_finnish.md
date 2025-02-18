# [Suomi] Debian Almquist Shell (dash) curl käyttö: Verkkopyynnön tekeminen

## Yleiskatsaus
Curl on komentorivityökalu, jota käytetään tiedostojen siirtämiseen verkon yli. Se tukee monia protokollia, kuten HTTP, HTTPS, FTP ja muita, ja se on erityisen hyödyllinen API-pyyntöjen tekemisessä.

## Käyttö
Perussyntaksi curl-komennolle on seuraava:

```bash
curl [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-X`: Määrittää HTTP-metodin (esim. GET, POST).
- `-d`: Lähettää tiedot POST-pyynnössä.
- `-H`: Lisää HTTP-otsikon pyyntöön.
- `-o`: Tallentaa vastauksen tiedostoon.
- `-I`: Hakee vain HTTP-otsikot.

## Yleiset esimerkit
### 1. Yksinkertainen GET-pyyntö
Hakee verkkosivun sisällön.

```bash
curl https://www.example.com
```

### 2. POST-pyyntö tietojen lähettämiseksi
Lähettää JSON-tietoja palvelimelle.

```bash
curl -X POST -d '{"key":"value"}' -H "Content-Type: application/json" https://www.example.com/api
```

### 3. Vastauksen tallentaminen tiedostoon
Tallentaa verkkosivun sisällön tiedostoon nimeltä `sivu.html`.

```bash
curl -o sivu.html https://www.example.com
```

### 4. HTTP-otsikoiden hakeminen
Hakee vain HTTP-otsikot verkkosivulta.

```bash
curl -I https://www.example.com
```

## Vinkit
- Käytä `-v` (verbose) -vaihtoehtoa saadaksesi lisätietoja pyynnöstä ja vastauksesta.
- Testaa API-pyyntöjä paikallisesti ennen tuotantoon siirtymistä.
- Varmista, että käytät HTTPS:ää, kun siirrät arkaluontoisia tietoja.