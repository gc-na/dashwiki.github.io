# [Suomi] Debian Almquist Shell (dash) tail käyttö: Näytä tiedoston loppu

## Yleiskatsaus
`tail`-komento on työkalu, jota käytetään tiedostojen viimeisten rivien näyttämiseen. Se on erityisen hyödyllinen lokitiedostojen tarkastelussa, joissa halutaan nähdä viimeisimmät tapahtumat tai tiedot.

## Käyttö
Perussyntaksi `tail`-komennolle on seuraava:

```bash
tail [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n [luku]`: Näyttää viimeiset [luku] riviä tiedostosta. Esimerkiksi `-n 10` näyttää viimeiset 10 riviä.
- `-f`: Seuraa tiedostoa reaaliaikaisesti ja näyttää uudet rivit, kun niitä lisätään. Tämä on hyödyllistä lokitiedostojen tarkastelussa.
- `-c [luku]`: Näyttää viimeiset [luku] tavua tiedostosta.

## Yleiset esimerkit
- Näytä viimeiset 10 riviä tiedostosta `esimerkki.txt`:

```bash
tail esimerkki.txt
```

- Näytä viimeiset 20 riviä tiedostosta `lokit.txt`:

```bash
tail -n 20 lokit.txt
```

- Seuraa lokitiedostoa `server.log` reaaliaikaisesti:

```bash
tail -f server.log
```

- Näytä viimeiset 100 tavua tiedostosta `data.bin`:

```bash
tail -c 100 data.bin
```

## Vinkit
- Käytä `-f`-vaihtoehtoa lokitiedostojen tarkastelussa, jotta pysyt ajan tasalla uusista tapahtumista.
- Voit yhdistää `tail`-komennon muihin komentoihin, kuten `grep`, suodataksesi vain tietyt rivit. Esimerkiksi:

```bash
tail -f server.log | grep "virhe"
```

- Muista, että `tail` näyttää tiedoston loppua, joten se ei muuta alkuperäistä tiedostoa.