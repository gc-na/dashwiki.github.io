# [Debian] Debian Almquist Shell (dash) sftp použití: Přenos souborů přes SSH

## Přehled
Příkaz `sftp` (Secure File Transfer Protocol) slouží k bezpečnému přenosu souborů mezi počítači přes SSH (Secure Shell). Umožňuje uživatelům nahrávat a stahovat soubory na vzdálené servery a spravovat soubory na těchto serverech.

## Použití
Základní syntaxe příkazu `sftp` je následující:

```bash
sftp [možnosti] [uživatel@hostitel]
```

## Běžné možnosti
- `-o` - specifikuje volby SSH, jako například port nebo identifikační klíč.
- `-b` - umožňuje provádět dávkové zpracování příkazů ze souboru.
- `-P` - určuje port pro připojení (pokud není standardní port 22).

## Běžné příklady
1. Připojení k vzdálenému serveru:
   ```bash
   sftp user@hostname
   ```

2. Stahování souboru ze vzdáleného serveru:
   ```bash
   sftp user@hostname:/remote/path/to/file /local/path/to/file
   ```

3. Nahrávání souboru na vzdálený server:
   ```bash
   sftp /local/path/to/file user@hostname:/remote/path/to/file
   ```

4. Použití dávkového režimu pro provedení více příkazů:
   ```bash
   sftp -b batchfile.txt user@hostname
   ```

## Tipy
- Při připojování k serveru se ujistěte, že máte správné uživatelské jméno a heslo.
- Pro zvýšení bezpečnosti používejte SSH klíče místo hesel.
- Vždy ověřte, že přenos souborů probíhá přes zabezpečené připojení, abyste ochránili citlivé údaje.