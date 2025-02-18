# [Danish] Debian Almquist Shell (dash) mount brug: Montering af filsystemer

## Oversigt
`mount`-kommandoen bruges til at montere filsystemer i Unix-lignende operativsystemer. Det gør det muligt for brugeren at tilgå filsystemer, der er gemt på forskellige enheder, som f.eks. harddiske, USB-drev eller netværksdrev.

## Brug
Den grundlæggende syntaks for `mount`-kommandoen er som følger:

```bash
mount [muligheder] [argumenter]
```

## Almindelige muligheder
- `-t type`: Angiver typen af filsystem, der skal monteres (f.eks. ext4, vfat).
- `-o options`: Angiver specifikke indstillinger for monteringen, såsom `ro` (read-only) eller `rw` (read-write).
- `-a`: Monterer alle filsystemer, der er angivet i `/etc/fstab`.
- `-r`: Monterer filsystemet som read-only.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `mount`-kommandoen kan bruges:

1. Montere et USB-drev:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Montere et netværksdrev med NFS:
   ```bash
   mount -t nfs 192.168.1.100:/share /mnt/nfs
   ```

3. Monter et filsystem som read-only:
   ```bash
   mount -o ro /dev/sda1 /mnt/data
   ```

4. Monter alle filsystemer fra `/etc/fstab`:
   ```bash
   mount -a
   ```

## Tips
- Sørg for, at du har de nødvendige rettigheder til at montere enheder. Du skal muligvis bruge `sudo`.
- Tjek altid, at den enhed, du vil montere, ikke allerede er monteret for at undgå konflikter.
- Brug `umount`-kommandoen til at afmontere filsystemer, når du er færdig med at bruge dem.