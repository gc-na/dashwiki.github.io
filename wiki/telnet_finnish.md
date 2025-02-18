# [Suomi] Debian Almquist Shell (dash) telnet käyttö: Verkkoyhteyksien testaaminen

## Yleiskatsaus
Telnet on komentorivipohjainen työkalu, jota käytetään verkkoyhteyksien testaamiseen ja hallintaan. Sen avulla käyttäjät voivat muodostaa yhteyden etäpalvelimiin ja käyttää niitä kuin olisivat paikallisella koneella.

## Käyttö
Perussyntaksi telnet-komennolle on seuraava:

```bash
telnet [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-l käyttäjätunnus`: Määrittää käyttäjätunnuksen, jota käytetään kirjautumiseen.
- `-f tiedosto`: Tallentaa telnet-istunnon lokitiedostoon.
- `-d`: Käynnistää telnetin debug-tilassa, mikä auttaa virheiden etsinnässä.

## Yleiset esimerkit
### Yhteyden muodostaminen palvelimeen
Voit muodostaa yhteyden etäpalvelimeen seuraavasti:

```bash
telnet example.com 80
```

### Yhteyden testaaminen
Voit testata, onko palvelin käytettävissä:

```bash
telnet localhost 22
```

### Lokitiedoston tallentaminen
Voit tallentaa telnet-istunnon lokitiedostoon:

```bash
telnet -f istunto.log example.com 80
```

## Vinkit
- Käytä telnetiä vain luotettavissa verkoissa, sillä se ei salaa tietoja.
- Varmista, että tiedät etäpalvelimen osoitteen ja portin ennen yhteyden muodostamista.
- Telnet on hyödyllinen työkalu, mutta harkitse turvallisempia vaihtoehtoja, kuten SSH, kun käytät etäyhteyksiä.