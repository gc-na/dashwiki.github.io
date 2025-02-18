# [Danish] Debian Almquist Shell (dash) umount brug: Aflukning af filsystemer

## Oversigt
`umount`-kommandoen bruges til at afmontere filsystemer, hvilket betyder at den fjerner forbindelsen mellem et filsystem og dets monteringspunkt. Dette er en vigtig operation for at sikre, at data bliver korrekt gemt, og at systemet forbliver stabilt.

## Brug
Den grundlæggende syntaks for `umount`-kommandoen er:

```sh
umount [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`: Afmonter alle monterede filsystemer, der er angivet i `/etc/mtab`.
- `-r`: Forsøg at afmontere filsystemet, og hvis det mislykkes, så mount det som skrivebeskyttet.
- `-f`: Tving afmontering, selvom filsystemet er optaget.
- `-l`: Udfør en "lazy" afmontering, som afmonterer filsystemet, når det ikke længere er i brug.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `umount` kan bruges:

1. Afmonter et specifikt filsystem:
   ```sh
   umount /mnt/usb
   ```

2. Afmonter alle filsystemer angivet i `/etc/mtab`:
   ```sh
   umount -a
   ```

3. Tving afmontering af et filsystem:
   ```sh
   umount -f /mnt/usb
   ```

4. Udfør en lazy afmontering:
   ```sh
   umount -l /mnt/usb
   ```

## Tips
- Sørg for at lukke alle åbne filer og terminaler, der bruger filsystemet, før du afmonterer det for at undgå datatab.
- Brug `mount`-kommandoen til at kontrollere, hvilke filsystemer der er monteret, før du afmonterer.
- Vær forsigtig med at bruge `-f` og `-l` mulighederne, da de kan føre til datatab, hvis filsystemet stadig er i brug.