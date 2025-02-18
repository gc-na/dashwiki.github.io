# [Suomi] Debian Almquist Shell (dash) ping6 käyttö: Verkon IPv6-yhteyksien testaaminen

## Yleiskatsaus
`ping6` on komento, jota käytetään IPv6-verkkojen yhteyksien testaamiseen. Se lähettää ICMPv6-viestejä (Internet Control Message Protocol for IPv6) kohdeosoitteeseen ja mittaa vasteaikaa, mikä auttaa selvittämään, onko verkko yhteydessä ja kuinka nopeasti se reagoi.

## Käyttö
Perussyntaksi `ping6`-komennolle on seuraava:
```bash
ping6 [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c [luku]`: Määrittää lähetettävien pakettien määrän.
- `-i [sekunnit]`: Asettaa viiveen pakettien lähettämisen väliin.
- `-w [sekunnit]`: Asettaa aikarajan komennon suorittamiselle.
- `-s [koko]`: Määrittää lähetettävän paketin koon tavuina.

## Yleiset esimerkit
### Yksinkertainen ping-osoite
Testaa yhteys tiettyyn IPv6-osoitteeseen:
```bash
ping6 2001:db8::1
```

### Rajoita lähetettävien pakettien määrää
Lähetä vain 5 pakettia:
```bash
ping6 -c 5 2001:db8::1
```

### Aseta pakettien koko
Lähetä 1000 tavun kokoisia paketteja:
```bash
ping6 -s 1000 2001:db8::1
```

### Aseta aikaraja
Aseta komennolle 10 sekunnin aikaraja:
```bash
ping6 -w 10 2001:db8::1
```

## Vinkit
- Käytä `-c`-vaihtoehtoa, jos haluat rajoittaa testin kestoa ja välttää liiallista verkon kuormitusta.
- Testaa useita eri IPv6-osoitteita varmistaaksesi, että verkko toimii oikein.
- Hyödynnä `-i`-vaihtoehtoa, jos haluat säätää pakettien lähetysväliä, erityisesti suurilla verkoilla.