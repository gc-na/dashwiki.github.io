# [Norsk] Debian Almquist Shell (dash) mount bruk: Montere filsystemer

## Oversikt
`mount`-kommandoen brukes til å montere filsystemer i Linux. Dette gjør det mulig å få tilgang til filer og kataloger som ligger på forskjellige lagringsenheter, som harddisker, USB-minnepinner eller nettverkslagring.

## Bruk
Grunnleggende syntaks for `mount`-kommandoen er som følger:

```
mount [alternativer] [argumenter]
```

## Vanlige alternativer
- `-t type`: Angir filsystemtypen (f.eks. ext4, ntfs).
- `-o alternativer`: Spesifiserer monteringsalternativer som `ro` (read-only) eller `rw` (read-write).
- `-a`: Monterer alle filsystemer som er spesifisert i `/etc/fstab`.
- `-v`: Viser detaljerte meldinger om monteringsprosessen.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `mount`-kommandoen:

1. Montere en USB-enhet:
   ```sh
   mount /dev/sdb1 /mnt/usb
   ```

2. Montere en NTFS-partisjon med skrivebeskyttelse:
   ```sh
   mount -t ntfs -o ro /dev/sdc1 /mnt/ntfs
   ```

3. Montere alle filsystemer fra `/etc/fstab`:
   ```sh
   mount -a
   ```

4. Montere en nettverksmappe (NFS):
   ```sh
   mount -t nfs server:/path/to/share /mnt/nfs
   ```

## Tips
- Sørg for at monteringspunktet (f.eks. `/mnt/usb`) eksisterer før du prøver å montere.
- Bruk `umount`-kommandoen for å avmontere filsystemer når du er ferdig med å bruke dem.
- Sjekk monterte filsystemer med `df -h` for å se tilgjengelig plass og monteringspunkter.