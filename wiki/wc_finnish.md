# [Suomi] Debian Almquist Shell (dash) wc käyttö: [laskentatyökalu tiedostojen sisältöön]

## Yleiskatsaus
`wc` (word count) on komentorivikäsky, joka laskee tiedostojen sisältöä. Se voi laskea sanojen, rivien ja merkkien määrän, mikä tekee siitä hyödyllisen työkalun tekstin analysoimiseen.

## Käyttö
Perussyntaksi `wc`-komennolle on seuraava:

```bash
wc [valinnat] [argumentit]
```

## Yleiset valinnat
- `-l`: Laskee vain rivien määrän.
- `-w`: Laskee vain sanojen määrän.
- `-c`: Laskee vain merkkien määrän.
- `-m`: Laskee merkkien määrän (UTF-8).
- `-L`: Näyttää pisimmän rivin pituuden.

## Yleiset esimerkit
Laske rivien, sanojen ja merkkien määrä tiedostosta `esimerkki.txt`:

```bash
wc esimerkki.txt
```

Laske vain rivien määrä:

```bash
wc -l esimerkki.txt
```

Laske vain sanojen määrä:

```bash
wc -w esimerkki.txt
```

Laske vain merkkien määrä:

```bash
wc -c esimerkki.txt
```

Laske usean tiedoston rivit, sanat ja merkit:

```bash
wc tiedosto1.txt tiedosto2.txt
```

## Vinkit
- Voit yhdistää `wc`-komennon muihin komentoihin putkella (`|`) saadaksesi tuloksia suoraan esimerkiksi `grep`-komennosta.
- Käytä `-m`-valintaa, jos työskentelet UTF-8-koodattujen tiedostojen kanssa, jotta saat tarkan merkkimäärän.
- Muista, että `wc` voi käsitellä useita tiedostoja kerralla, mikä helpottaa suurten tietomäärien analysoimista.