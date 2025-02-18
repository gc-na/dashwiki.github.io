# [Suomi] Debian Almquist Shell (dash) netstat käyttö: Verkkoyhteyksien tarkastelu

## Yleiskatsaus
`netstat`-komento on työkalu, jota käytetään verkkoyhteyksien, reititystaulukoiden ja verkkoprotokollien tilan tarkasteluun. Se tarjoaa tietoa aktiivisista yhteyksistä ja niiden tilasta, mikä on hyödyllistä verkon hallinnassa ja vianetsinnässä.

## Käyttö
Perussyntaksi `netstat`-komennolle on seuraava:

```bash
netstat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`: Näyttää kaikki yhteydet ja kuunteluportit.
- `-t`: Näyttää vain TCP-yhteydet.
- `-u`: Näyttää vain UDP-yhteydet.
- `-n`: Näyttää osoitteet ja portit numeerisessa muodossa.
- `-l`: Näyttää vain kuunteluyhteydet.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `netstat`-komennon käytöstä:

1. Näytä kaikki aktiiviset yhteydet:
   ```bash
   netstat -a
   ```

2. Näytä vain TCP-yhteydet:
   ```bash
   netstat -t
   ```

3. Näytä vain UDP-yhteydet:
   ```bash
   netstat -u
   ```

4. Näytä yhteydet numeerisessa muodossa:
   ```bash
   netstat -n
   ```

5. Näytä vain kuunteluyhteydet:
   ```bash
   netstat -l
   ```

## Vinkit
- Käytä `-n`-vaihtoehtoa, jos haluat nopeamman tulosteen, koska se ohittaa DNS-nimien selvittämisen.
- Yhdistä useita vaihtoehtoja, kuten `netstat -tunl`, saadaksesi kattavan näkymän TCP- ja UDP-yhteyksistä, jotka ovat kuuntelutilassa.
- Tarkista säännöllisesti verkkoyhteyksien tila, erityisesti palvelimilla, joilla on paljon liikennettä, jotta voit havaita mahdolliset ongelmat ajoissa.