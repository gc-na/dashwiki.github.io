# [Suomi] Debian Almquist Shell (dash) ss käyttö: verkko- ja yhteystietojen tarkastelu

## Yleiskatsaus
`ss`-komento on työkalu, jota käytetään verkko- ja yhteystietojen tarkasteluun Linux-järjestelmissä. Se tarjoaa tietoa avoimista yhteyksistä, kuuntelevista porteista ja muista verkko-ongelmista, ja se on tehokas vaihtoehto vanhemmalle `netstat`-komennolle.

## Käyttö
Perussyntaksi `ss`-komennolle on seuraava:

```bash
ss [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-t`: Näyttää TCP-yhteydet.
- `-u`: Näyttää UDP-yhteydet.
- `-l`: Näyttää vain kuuntelevat yhteydet.
- `-p`: Näyttää prosessin, joka käyttää yhteyttä.
- `-n`: Näyttää numeromuotoiset osoitteet ja portit (ilman DNS-nimiä).

## Yleiset esimerkit
1. **Näytä kaikki avoimet TCP-yhteydet:**

    ```bash
    ss -t
    ```

2. **Näytä kaikki kuuntelevat portit:**

    ```bash
    ss -l
    ```

3. **Näytä kaikki UDP-yhteydet:**

    ```bash
    ss -u
    ```

4. **Näytä TCP-yhteydet prosessitietojen kanssa:**

    ```bash
    ss -tp
    ```

5. **Näytä kaikki yhteydet numeromuodossa:**

    ```bash
    ss -n
    ```

## Vinkit
- Käytä `-p`-vaihtoehtoa, jos haluat nähdä, mikä prosessi käyttää tiettyä yhteyttä. Tämä voi olla hyödyllistä ongelmien ratkaisemisessa.
- Yhdistä useita vaihtoehtoja, kuten `ss -tunlp`, saadaksesi kattavan näkymän kaikista yhteyksistä ja niiden prosesseista.
- Muista, että `ss`-komento vaatii usein root-oikeudet, jotta voit nähdä kaikki prosessit ja yhteydet.