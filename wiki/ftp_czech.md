# [Český] Debian Almquist Shell (dash) ftp použití: Přenos souborů přes FTP

## Přehled
Příkaz `ftp` se používá k přenosu souborů mezi počítačem a serverem pomocí protokolu FTP (File Transfer Protocol). Umožňuje uživatelům připojit se k FTP serveru, procházet soubory a nahrávat nebo stahovat soubory.

## Použití
Základní syntaxe příkazu `ftp` je následující:

```bash
ftp [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Vypne interaktivní režim, což znamená, že se nebudou ptát na potvrzení při přenosu souborů.
- `-n`: Zabrání automatickému přihlášení k FTP serveru.
- `-v`: Zobrazí podrobné informace o přenosu.
- `-p`: Používá pasivní režim pro připojení k FTP serveru.

## Běžné příklady
1. Připojení k FTP serveru:
   ```bash
   ftp ftp.example.com
   ```

2. Připojení k FTP serveru s uživatelským jménem:
   ```bash
   ftp -n ftp.example.com
   ```

3. Nahrání souboru na server:
   ```bash
   put soubor.txt
   ```

4. Stažení souboru ze serveru:
   ```bash
   get soubor.txt
   ```

5. Zobrazení seznamu souborů na serveru:
   ```bash
   ls
   ```

## Tipy
- Při přenosu velkých souborů zvažte použití příkazu `-i`, abyste se vyhnuli zbytečným potvrzením.
- Pokud máte problémy s připojením, zkuste použít pasivní režim pomocí příkazu `-p`.
- Nezapomeňte se odhlásit z FTP serveru pomocí příkazu `bye` nebo `quit`, abyste ukončili relaci správně.