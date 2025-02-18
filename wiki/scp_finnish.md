# [Suomi] Debian Almquist Shell (dash) scp käyttö: Tiedostojen siirto turvallisesti

## Yleiskatsaus
`scp` (Secure Copy Protocol) on komentorivikäsky, jota käytetään tiedostojen siirtämiseen turvallisesti paikalliselta koneelta etäkoneelle tai päinvastoin. Se hyödyntää SSH-protokollaa tiedonsiirron salaamiseen, mikä tekee siitä turvallisen vaihtoehdon tiedostojen siirtämiseen verkossa.

## Käyttö
Perussyntaksi `scp`-komennolle on seuraava:

```bash
scp [vaihtoehdot] [lähde] [kohde]
```

## Yleiset vaihtoehdot
- `-r`: Siirtää hakemiston ja sen sisällön rekursiivisesti.
- `-P`: Määrittää etäpalvelimen portin (huomaa, että iso P).
- `-i`: Määrittää yksityisen avaimen tiedoston, jota käytetään SSH-yhteyden muodostamiseen.
- `-v`: Näyttää yksityiskohtaista tietoa siirrosta (debugging-tilassa).

## Yleiset esimerkit
Siirretään tiedosto paikalliselta koneelta etäkoneelle:

```bash
scp localfile.txt user@remotehost:/path/to/destination/
```

Siirretään tiedosto etäkoneelta paikalliselle koneelle:

```bash
scp user@remotehost:/path/to/remotefile.txt /local/destination/
```

Siirretään hakemisto rekursiivisesti etäkoneelle:

```bash
scp -r localdirectory/ user@remotehost:/path/to/destination/
```

Määritetään portti siirron aikana:

```bash
scp -P 2222 localfile.txt user@remotehost:/path/to/destination/
```

## Vinkit
- Varmista, että SSH-yhteys toimii ennen `scp`-komennon käyttöä.
- Käytä `-v`-vaihtoehtoa, jos kohtaat ongelmia siirron aikana, jotta saat lisätietoja virheistä.
- Muista, että tiedostojen siirto voi kestää aikaa, erityisesti suurten tiedostojen tai heikon verkkoyhteyden kanssa.