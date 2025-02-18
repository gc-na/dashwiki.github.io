# [Suomi] Debian Almquist Shell (dash) strace käyttö: Ohjelman järjestelmäkutsujen jäljittäminen

## Yleiskatsaus
`strace` on työkalu, jota käytetään ohjelmien järjestelmäkutsujen ja signaalien jäljittämiseen. Se auttaa kehittäjiä ja järjestelmänvalvojia ymmärtämään, mitä ohjelma tekee taustalla, ja se voi olla erityisen hyödyllinen virheiden etsinnässä.

## Käyttö
Perussyntaksi `strace`-komennolle on seuraava:

```bash
strace [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Laskee järjestelmäkutsujen määrät ja niiden keston.
- `-e`: Suodattaa näkyviin vain tietyt järjestelmäkutsut.
- `-o tiedosto`: Tallentaa jäljitystiedot annettuun tiedostoon.
- `-p prosessi`: Jäljittää jo käynnissä olevaa prosessia, jonka prosessitunnus (PID) on annettu.
- `-f`: Jäljittää myös lapsiprosessit.

## Yleiset esimerkit
### Peruskomennon jäljittäminen
Voit jäljittää yksinkertaista komentoa, kuten `ls`, seuraavasti:

```bash
strace ls
```

### Järjestelmäkutsujen laskeminen
Jos haluat nähdä, kuinka monta kertaa kukin järjestelmäkutsu suoritettiin, käytä `-c`-vaihtoehtoa:

```bash
strace -c ls
```

### Tietojen tallentaminen tiedostoon
Voit tallentaa jäljitystiedot tiedostoon käyttämällä `-o`-vaihtoehtoa:

```bash
strace -o strace_output.txt ls
```

### Jo käynnissä olevan prosessin jäljittäminen
Jos haluat jäljittää jo käynnissä olevaa prosessia, käytä `-p`-vaihtoehtoa ja anna prosessitunnus:

```bash
strace -p 1234
```

### Tiettyjen järjestelmäkutsujen suodattaminen
Voit suodattaa näkyviin vain tietyt kutsut, esimerkiksi `open`:

```bash
strace -e trace=open ls
```

## Vinkit
- Käytä `-o`-vaihtoehtoa tallentaaksesi tulokset tiedostoon, jolloin voit analysoida niitä myöhemmin.
- Suodata kutsuja `-e`-vaihtoehdolla, jotta saat tarkempaa tietoa vain kiinnostavista toiminnoista.
- Muista, että `strace` voi hidastaa ohjelman suoritusta, joten käytä sitä vain tarvittaessa.
- Hyödynnä `-c`-vaihtoehtoa saadaksesi nopean yhteenvedon ohjelman suorituskyvystä.