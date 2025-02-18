# [Suomi] Debian Almquist Shell (dash) netcat käyttö: Verkkoyhteyksien hallinta

## Yleiskatsaus
Netcat, usein kutsuttu "internetin sveitsiläiseksi armeijaveitseksi", on monipuolinen työkalu, jota käytetään verkkoyhteyksien luomiseen ja hallintaan. Se mahdollistaa tietojen siirron TCP- tai UDP-protokollien avulla ja voi toimia sekä palvelimena että asiakkaana.

## Käyttö
Perussyntaksi netcat-komennolle on seuraava:

```bash
netcat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l`: Kuuntelee saapuvia yhteyksiä (palvelin).
- `-p [portti]`: Määrittää portin, jota käytetään.
- `-u`: Käyttää UDP-protokollaa TCP:n sijaan.
- `-v`: Näyttää yksityiskohtaisempaa tietoa (verbose).
- `-z`: Skannaa portteja ilman yhteyden muodostamista (zero-I/O mode).

## Yleiset esimerkit
### Yhteyden luominen palvelimeen
Voit luoda yhteyden etäpalvelimeen ja porttiin seuraavasti:

```bash
netcat example.com 80
```

### Palvelimen kuuntelu
Voit asettaa netcatin kuuntelemaan tiettyä porttia:

```bash
netcat -l -p 1234
```

### Tiedostojen siirto
Voit siirtää tiedoston etäpalvelimelle:

Lähettäjäpuolella:

```bash
netcat -l -p 1234 < tiedosto.txt
```

Vastaanottajapuolella:

```bash
netcat lähettäjä_ip 1234 > vastaanotettu_tiedosto.txt
```

### Porttiskannaus
Voit skannata portteja etäpalvelimella:

```bash
netcat -z -v example.com 1-100
```

## Vinkit
- Käytä `-v`-vaihtoehtoa virheiden ja yhteyden muodostamisen tarkistamiseen.
- Varmista, että palomuuriasetukset sallivat netcatin käytön.
- Netcat voi olla vaarallinen työkalu, joten käytä sitä vain luotettavissa ympäristöissä ja varmista, että sinulla on lupa käyttää sitä.