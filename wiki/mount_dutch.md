# [Nederlands] Debian Almquist Shell (dash) mount gebruik: Schijfpartities koppelen

## Overzicht
De `mount`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om bestandssystemen te koppelen aan een bepaalde map in de bestandsstructuur van het systeem. Dit stelt gebruikers in staat om toegang te krijgen tot de gegevens op verschillende opslagapparaten, zoals harde schijven, USB-sticks of netwerkschijven.

## Gebruik
De basis syntaxis van de `mount`-opdracht is als volgt:

```sh
mount [opties] [apparaat] [punt]
```

Hierbij is `[apparaat]` het opslagmedium dat je wilt koppelen en `[punt]` de map waar je het bestandssysteem wilt koppelen.

## Veelvoorkomende Opties
- `-t type`: Specificeert het type bestandssysteem (bijvoorbeeld `ext4`, `ntfs`, etc.).
- `-o opties`: Geeft extra opties op, zoals `ro` (alleen-lezen) of `rw` (lees- en schrijfmodus).
- `-a`: Koppelt alle bestandssystemen die in `/etc/fstab` zijn gedefinieerd.
- `-r`: Koppelt het bestandssysteem in alleen-lezen modus.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mount`-opdracht:

1. **Koppelen van een USB-stick**:
   ```sh
   mount /dev/sdb1 /mnt/usb
   ```

2. **Koppelen met een specifiek bestandssysteemtype**:
   ```sh
   mount -t ext4 /dev/sda1 /mnt/data
   ```

3. **Koppelen in alleen-lezen modus**:
   ```sh
   mount -o ro /dev/sr0 /mnt/cdrom
   ```

4. **Koppelen van alle bestandssystemen in fstab**:
   ```sh
   mount -a
   ```

## Tips
- Zorg ervoor dat je de juiste machtigingen hebt om een apparaat te koppelen; je hebt vaak root-toegang nodig.
- Controleer altijd of het apparaat niet al is gekoppeld om fouten te voorkomen.
- Vergeet niet om het bestandssysteem weer los te koppelen met de `umount`-opdracht wanneer je klaar bent.