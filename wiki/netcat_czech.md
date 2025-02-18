# [Český] Debian Almquist Shell (dash) netcat použití: Nástroj pro síťovou komunikaci

## Přehled
Netcat, často označovaný jako "kapesní nůž" pro síťovou komunikaci, je nástroj, který umožňuje číst a zapisovat data přes síťové spojení pomocí protokolů TCP nebo UDP. Je užitečný pro testování a diagnostiku síťových služeb.

## Použití
Základní syntaxe příkazu netcat je následující:

```
netcat [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Naslouchá na zadaném portu.
- `-p [port]`: Určuje port, na kterém má netcat naslouchat nebo se připojit.
- `-u`: Používá UDP místo TCP.
- `-v`: Aktivuje podrobné výstupy (verbose).
- `-z`: Provádí skenování portů bez přenosu dat.

## Běžné příklady
1. **Naslouchání na portu 1234:**
   ```bash
   netcat -l -p 1234
   ```

2. **Připojení k serveru na portu 80:**
   ```bash
   netcat example.com 80
   ```

3. **Odeslání souboru přes netcat:**
   ```bash
   netcat -l -p 1234 > soubor.txt
   ```
   Na druhém terminálu:
   ```bash
   netcat localhost 1234 < soubor.txt
   ```

4. **Skenování portů na cílovém hostiteli:**
   ```bash
   netcat -z -v example.com 1-1000
   ```

## Tipy
- Používejte `-v` pro získání více informací o tom, co netcat dělá, což může být užitečné při ladění.
- Při přenosu souborů se ujistěte, že na obou stranách používáte stejný port a že je port otevřený.
- Netcat může být použit jako jednoduchý server pro testování, což je užitečné pro vývojáře a administrátory.