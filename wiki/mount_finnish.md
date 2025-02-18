# [Suomi] Debian Almquist Shell (dash) mount käyttö: Liitä tiedostojärjestelmiä

## Yleiskatsaus
`mount`-komento käytetään tiedostojärjestelmien liittämiseen Unix-pohjaisissa käyttöjärjestelmissä, kuten Debianissa. Sen avulla voit liittää tiedostojärjestelmiä, kuten kiintolevyjä tai USB-muistitikkuja, järjestelmään, jolloin voit käyttää niiden sisältöä.

## Käyttö
Perussyntaksi `mount`-komennolle on seuraava:

```bash
mount [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-t tyyppi`: Määrittää liitettävän tiedostojärjestelmän tyypin (esim. ext4, vfat).
- `-o vaihtoehdot`: Määrittää lisävaihtoehtoja, kuten `ro` (vain luku) tai `rw` (luku/kirjoitus).
- `-a`: Liittää kaikki tiedostojärjestelmät, jotka on määritelty `/etc/fstab`-tiedostossa.

## Yleiset esimerkit
### 1. Tiedostojärjestelmän liittäminen
Liitä esimerkiksi USB-muistitikku, joka on `/dev/sdb1`, hakemistoon `/mnt/usb`:

```bash
mount /dev/sdb1 /mnt/usb
```

### 2. Tiedostojärjestelmän liittäminen tietyllä tyypillä
Liitä FAT32-tiedostojärjestelmä:

```bash
mount -t vfat /dev/sdb1 /mnt/usb
```

### 3. Liittäminen vain luku -tilassa
Liitä tiedostojärjestelmä vain luku -tilassa:

```bash
mount -o ro /dev/sdb1 /mnt/usb
```

### 4. Kaikkien tiedostojärjestelmien liittäminen
Liitä kaikki tiedostojärjestelmät, jotka on määritelty `/etc/fstab`-tiedostossa:

```bash
mount -a
```

## Vinkit
- Varmista, että kohdehakemisto (esim. `/mnt/usb`) on olemassa ennen liittämistä.
- Tarkista liitetyt tiedostojärjestelmät komennolla `df -h`.
- Muista irrottaa tiedostojärjestelmä ennen sen poistamista käyttämällä `umount`-komentoa.