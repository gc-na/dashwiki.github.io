# [Suomi] Debian Almquist Shell (dash) ping käyttö: Verkon yhteyden testaaminen

## Yleiskatsaus
Ping-komento on työkalu, jota käytetään verkon yhteyksien testaamiseen. Se lähettää ICMP-echo-pyyntöjä määritettyyn osoitteeseen ja mittaa, kuinka kauan kestää saada vastaus. Tämä auttaa selvittämään, onko kohde saavutettavissa ja kuinka hyvin se reagoi.

## Käyttö
Perussyntaksi ping-komennolle on seuraava:

```
ping [vaihtoehdot] [osoite]
```

## Yleiset vaihtoehdot
- `-c [luku]`: Määrittää, kuinka monta pyyntöä lähetetään.
- `-i [aika]`: Asettaa viiveen pyyntöjen välillä sekunteina.
- `-s [koko]`: Määrittää lähetettävän datan koon tavuina.
- `-t`: Jatkaa pyyntöjen lähettämistä, kunnes se keskeytetään manuaalisesti.

## Yleiset esimerkit
### 1. Yhteyden testaaminen
Yksinkertainen ping-komento, joka testaa yhteyden google.comiin:

```
ping google.com
```

### 2. Rajoita pyyntöjen määrää
Pingaa google.com ja lähetä vain 4 pyyntöä:

```
ping -c 4 google.com
```

### 3. Määritä viive pyyntöjen välillä
Pingaa osoitetta 8.8.8.8, ja aseta viive 2 sekuntia pyyntöjen välille:

```
ping -i 2 8.8.8.8
```

### 4. Muuta datan kokoa
Pingaa osoitetta ja lähetä 100 tavun kokoisia paketteja:

```
ping -s 100 google.com
```

## Vinkit
- Käytä `-c`-vaihtoehtoa, jos haluat rajoittaa pyyntöjen määrää, jotta et kuormita verkkoa liikaa.
- Ping-komennon tulokset voivat auttaa diagnosoimaan verkko-ongelmia, kuten viiveitä tai katkoja.
- Muista, että jotkut palvelimet voivat estää ping-pyynnöt turvallisuussyistä, joten kaikki pyyntösi eivät välttämättä onnistu.