# [Český] Debian Almquist Shell (dash) mount použití: Připojení souborových systémů

## Přehled
Příkaz `mount` slouží k připojení souborových systémů k určitému bodu v adresářové struktuře. Umožňuje uživatelům přistupovat k datům na různých zařízeních, jako jsou pevné disky, USB flash disky nebo síťové disky.

## Použití
Základní syntaxe příkazu `mount` je následující:

```sh
mount [možnosti] [argumenty]
```

## Běžné možnosti
- `-t <typ>`: Určuje typ souborového systému (např. ext4, ntfs).
- `-o <možnosti>`: Specifikuje další možnosti připojení, jako jsou `ro` (pouze pro čtení) nebo `rw` (čtení a zápis).
- `-a`: Připojí všechny souborové systémy uvedené v souboru `/etc/fstab`.
- `-r`: Připojí souborový systém pouze pro čtení.

## Běžné příklady
Připojení ext4 souborového systému z pevného disku:

```sh
mount -t ext4 /dev/sda1 /mnt/mydisk
```

Připojení USB flash disku s možností pouze pro čtení:

```sh
mount -o ro /dev/sdb1 /mnt/usb
```

Připojení všech souborových systémů podle `/etc/fstab`:

```sh
mount -a
```

Připojení NTFS disku s možnostmi pro čtení a zápis:

```sh
mount -t ntfs-3g -o rw /dev/sdc1 /mnt/ntfsdisk
```

## Tipy
- Před připojením se ujistěte, že cílový adresář (např. `/mnt/mydisk`) existuje.
- Používejte příkaz `umount` pro bezpečné odpojení souborového systému, abyste předešli ztrátě dat.
- Zkontrolujte, zda máte potřebná oprávnění pro připojení souborového systému, obvykle je vyžadováno administrátorské oprávnění (root).