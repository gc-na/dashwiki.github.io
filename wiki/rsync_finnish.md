# [Suomi] Debian Almquist Shell (dash) rsync käyttö: Tiedostojen synkronointi ja siirto

## Yleiskatsaus
Rsync on tehokas komento tiedostojen synkronointiin ja siirtoon paikallisesti tai etäpalvelimille. Se mahdollistaa tiedostojen ja hakemistojen kopioimisen ja synkronoinnin tehokkaasti vain muuttuneiden osien perusteella.

## Käyttö
Rsyncin perussyntaksi on seuraava:

```bash
rsync [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`: Arkistointitila, joka säilyttää tiedostojen ominaisuudet (oikeudet, aikaleimat jne.).
- `-v`: Näytä yksityiskohtainen tulostus siirron aikana.
- `-z`: Pakkaa tiedostot siirron aikana, mikä voi nopeuttaa siirtoa hitaissa yhteyksissä.
- `-r`: Kopioi hakemistot rekursiivisesti.
- `--delete`: Poistaa kohdekansiosta tiedostot, joita ei enää ole lähdekansiossa.

## Yleiset esimerkit
### Tiedostojen kopioiminen paikallisesti
Kopioi tiedosto `file.txt` nykyisestä hakemistosta toiseen hakemistoon `backup/`:

```bash
rsync -av file.txt backup/
```

### Hakemiston synkronointi etäpalvelimelle
Synkronoi paikallinen hakemisto `myfolder/` etäpalvelimelle `user@remote:/path/to/destination/`:

```bash
rsync -avz myfolder/ user@remote:/path/to/destination/
```

### Tiedostojen siirto ja poistaminen
Siirrä tiedostot `source/` hakemistosta `destination/` ja poista kohdekansiosta tiedostot, joita ei enää ole lähteessä:

```bash
rsync -av --delete source/ destination/
```

## Vinkit
- Käytä `-n` (tai `--dry-run`) -vaihtoehtoa testataksesi, mitä rsync tekisi ilman varsinaista siirtoa.
- Varmista, että käytät oikeita polkuja, erityisesti etäpalvelimilla, jotta tiedostot siirtyvät oikeisiin paikkoihin.
- Hyödynnä `--progress` -vaihtoehtoa nähdäksesi siirron edistymisen reaaliajassa.