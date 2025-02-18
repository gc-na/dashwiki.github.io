# [Suomi] Debian Almquist Shell (dash) wget käyttö: Tiedostojen lataaminen verkosta

## Yleiskatsaus
`wget` on komentorivipohjainen työkalu, jota käytetään tiedostojen lataamiseen verkosta. Se tukee useita protokollia, kuten HTTP, HTTPS ja FTP, ja se on erityisen hyödyllinen suurten tiedostojen lataamiseen tai verkkosivustojen peilaamiseen.

## Käyttö
Perussyntaksi `wget`-komennolle on seuraava:

```bash
wget [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-O [tiedostonimi]`: Määrittää ladattavan tiedoston nimen.
- `-c`: Jatkaa keskeytettyä latausta.
- `-q`: Suorittaa hiljaisen latauksen, jolloin ei näytetä lataustietoja.
- `--limit-rate=[nopeus]`: Rajoittaa latausnopeuden.
- `-r`: Lataa verkkosivuston rekursiivisesti.

## Yleiset esimerkit
### Peruslataus
Lataa tiedosto suoraan URL-osoitteesta:
```bash
wget http://esimerkki.com/tiedosto.txt
```

### Tiedoston nimeäminen
Lataa tiedosto ja nimeä se toisin:
```bash
wget -O uusi_tiedosto.txt http://esimerkki.com/tiedosto.txt
```

### Keskeytetyn latauksen jatkaminen
Jos lataus keskeytyy, voit jatkaa sitä näin:
```bash
wget -c http://esimerkki.com/suuri_tiedosto.zip
```

### Hiljainen lataus
Lataa tiedosto ilman lataustietojen näyttämistä:
```bash
wget -q http://esimerkki.com/tiedosto.txt
```

### Verkkosivuston peilaaminen
Lataa koko verkkosivusto rekursiivisesti:
```bash
wget -r http://esimerkki.com
```

## Vinkit
- Käytä `-c`-vaihtoehtoa suurten tiedostojen lataamisessa, jotta voit jatkaa keskeytettyjä latauksia.
- Rajoita latausnopeutta `--limit-rate`-vaihtoehdolla, jos verkko on hidas tai haluat säästää kaistaa.
- Hyödynnä `-q`-vaihtoehtoa, kun haluat suorittaa latauksia taustalla ilman häiriöitä.