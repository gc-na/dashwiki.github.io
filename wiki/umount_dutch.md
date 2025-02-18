# [Nederlands] Debian Almquist Shell (dash) umount gebruik: Verwijder een gemonteerde bestandssysteem

## Overzicht
De `umount`-opdracht wordt gebruikt om een gemonteerd bestandssysteem te ontkoppelen. Dit is belangrijk om ervoor te zorgen dat gegevens veilig worden opgeslagen en dat het bestandssysteem niet meer toegankelijk is voor verdere bewerkingen.

## Gebruik
De basis syntaxis van de `umount`-opdracht is als volgt:

```bash
umount [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Ontkoppel alle gemonteerde bestandssystemen die in `/etc/mtab` zijn vermeld.
- `-f`: Forceer het ontkoppelen, zelfs als het bestandssysteem druk is.
- `-l`: Ontkoppel het bestandssysteem 'lazily', wat betekent dat het ontkoppelen wordt uitgesteld totdat het niet meer in gebruik is.
- `-r`: Probeer het bestandssysteem alleen-lezen te maken als het niet kan worden ontkoppeld.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `umount`-opdracht:

1. Ontkoppel een bestandssysteem op basis van het pad:
   ```bash
   umount /mnt/usb
   ```

2. Ontkoppel een bestandssysteem op basis van de apparaatnaam:
   ```bash
   umount /dev/sdb1
   ```

3. Forceer het ontkoppelen van een bestandssysteem:
   ```bash
   umount -f /mnt/usb
   ```

4. Ontkoppel alle gemonteerde bestandssystemen:
   ```bash
   umount -a
   ```

5. Ontkoppel een bestandssysteem 'lazily':
   ```bash
   umount -l /mnt/usb
   ```

## Tips
- Zorg ervoor dat je geen bestanden opent of processen uitvoert die het bestandssysteem gebruiken voordat je het ontkoppelt.
- Gebruik de `-l` optie als je een bestandssysteem wilt ontkoppelen dat momenteel in gebruik is, maar je wilt niet dat het onmiddellijk gebeurt.
- Controleer altijd of het bestandssysteem succesvol is ontkoppeld door de `mount`-opdracht zonder argumenten uit te voeren en te kijken of het bestandssysteem niet meer wordt weergegeven.