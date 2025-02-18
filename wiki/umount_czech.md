# [Český] Debian Almquist Shell (dash) umount: Odpojení souborového systému

## Přehled
Příkaz `umount` slouží k odpojení souborového systému, který byl předtím připojen pomocí příkazu `mount`. Tento příkaz je důležitý pro správu souborových systémů a zajišťuje, že data jsou správně uložena a že zařízení je bezpečně odpojeno.

## Použití
Základní syntaxe příkazu `umount` je následující:

```bash
umount [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Odpojí všechny souborové systémy uvedené v `/etc/mtab`.
- `-f`: Vynutí odpojení souborového systému, i když je stále používán.
- `-l`: Odpojí souborový systém "lazy", což znamená, že se odpojení provede, jakmile přestanou být používány všechny otevřené soubory.
- `-r`: Pokud dojde k chybě při odpojení, pokusí se souborový systém připojit zpět.

## Běžné příklady
1. Odpojení konkrétního souborového systému:
   ```bash
   umount /mnt/usb
   ```

2. Odpojení všech souborových systémů:
   ```bash
   umount -a
   ```

3. Vynucené odpojení souborového systému:
   ```bash
   umount -f /mnt/usb
   ```

4. Lazy odpojení souborového systému:
   ```bash
   umount -l /mnt/usb
   ```

## Tipy
- Před odpojením souborového systému se ujistěte, že na něm nejsou otevřené soubory, aby nedošlo k poškození dat.
- Používejte volbu `-l` pro bezpečné odpojení, pokud máte obavy z aktivních procesů.
- Vždy zkontrolujte, zda je souborový systém úspěšně odpojen, pomocí příkazu `mount` nebo `df`.