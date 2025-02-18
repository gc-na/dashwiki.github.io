# [Svenska] Debian Almquist Shell (dash) mount användning: Montera filsystem

## Översikt
Kommandot `mount` används för att montera filsystem i Unix-liknande operativsystem. Genom att använda detta kommando kan du ansluta ett filsystem från en enhet, som en hårddisk eller USB-minne, till en specifik plats i filsystemstrukturen så att du kan komma åt dess innehåll.

## Användning
Den grundläggande syntaxen för kommandot `mount` ser ut så här:

```bash
mount [alternativ] [enhet] [monteringspunkt]
```

## Vanliga alternativ
- `-t` : Specifierar typ av filsystem (t.ex. ext4, vfat).
- `-o` : Anger specifika alternativ för monteringen, som `ro` (read-only) eller `rw` (read-write).
- `-a` : Monterar alla filsystem som är angivna i `/etc/fstab`.
- `-r` : Monterar filsystemet som skrivskyddat.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda kommandot `mount`:

1. Montera en USB-enhet:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Montera ett ext4-filsystem med specifika alternativ:
   ```bash
   mount -t ext4 -o rw /dev/sda1 /mnt/data
   ```

3. Monterar alla filsystem från `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Montera en ISO-fil:
   ```bash
   mount -o loop /path/to/image.iso /mnt/iso
   ```

## Tips
- Kontrollera alltid att du har rätt behörigheter för att montera en enhet.
- Använd `umount` för att avmontera filsystemet när du är klar, för att säkerställa att inga data går förlorade.
- Kontrollera med `df -h` för att se vilka filsystem som är monterade och deras användning.