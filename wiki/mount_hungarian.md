# [Linux] Debian Almquist Shell (dash) mount használata: Fájl rendszerek csatolása

## Áttekintés
A `mount` parancs lehetővé teszi a fájlrendszerek csatolását a Linux operációs rendszerekben. Ezzel a paranccsal csatlakoztathatunk különböző tárolóeszközöket, például USB meghajtókat vagy partíciókat a rendszerhez, így azok elérhetővé válnak a fájlkezelők és a parancssor számára.

## Használat
A `mount` parancs alapvető szintaxisa a következő:

```bash
mount [opciók] [argumentumok]
```

## Gyakori Opciók
- `-t <típus>`: Meghatározza a fájlrendszer típusát (pl. ext4, ntfs).
- `-o <opciók>`: Speciális opciók megadása a csatoláshoz (pl. `ro` a csak olvasható csatlakozáshoz).
- `-a`: Minden fájlrendszer csatolása a /etc/fstab fájl alapján.

## Gyakori Példák
1. **Fájl rendszer csatolása alapértelmezett beállításokkal:**
   ```bash
   mount /dev/sdb1 /mnt/mydrive
   ```

2. **Csak olvasható csatolás:**
   ```bash
   mount -o ro /dev/sdb1 /mnt/mydrive
   ```

3. **Fájl rendszer csatolása megadott típussal:**
   ```bash
   mount -t ntfs /dev/sdc1 /mnt/windows
   ```

4. **Minden fájlrendszer csatolása a fstab fájl alapján:**
   ```bash
   mount -a
   ```

## Tippek
- Mindig ellenőrizd, hogy a csatolni kívánt eszköz nem használatban van-e, mielőtt megpróbálnád csatolni.
- Használj `df -h` parancsot a csatolt fájlrendszerek ellenőrzésére.
- Ne felejtsd el a csatolt fájlrendszert leválasztani a `umount` paranccsal, mielőtt fizikailag eltávolítanád az eszközt.