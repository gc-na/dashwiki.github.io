# [Debian] Debian Almquist Shell (dash) socat použití: Přesměrování a manipulace s datovými proudy

## Přehled
Příkaz `socat` (Socket CAT) je mocný nástroj pro přesměrování a manipulaci s datovými proudy. Umožňuje vytvářet spojení mezi různými typy datových kanálů, jako jsou síťové sockety, soubory, terminály a další. Je užitečný pro testování, ladění a přenos dat mezi různými aplikacemi.

## Použití
Základní syntaxe příkazu `socat` je následující:

```bash
socat [možnosti] [argumenty]
```

## Běžné možnosti
- `-u`: Použít neblokující režim.
- `-v`: Zobrazit podrobné informace o přenášených datech.
- `-d`: Aktivovat ladící výstup pro diagnostiku.
- `TCP:<host>:<port>`: Připojit se k TCP serveru na zadaném hostu a portu.
- `UDP:<host>:<port>`: Připojit se k UDP serveru na zadaném hostu a portu.

## Běžné příklady
1. **Přesměrování dat mezi dvěma porty:**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:localhost:5678
   ```

2. **Přenos dat mezi souborem a TCP socketem:**
   ```bash
   socat TCP-LISTEN:1234,fork FILE:/tmp/myfile.txt,creat
   ```

3. **Zobrazení dat z terminálu na TCP socket:**
   ```bash
   socat -v - TCP:localhost:1234
   ```

4. **Odesílání dat z jednoho UDP portu na druhý:**
   ```bash
   socat UDP-LISTEN:1234,fork UDP:localhost:5678
   ```

## Tipy
- Při práci s `socat` je dobré používat možnost `-v` pro sledování přenášených dat, což může pomoci při ladění.
- Ujistěte se, že máte správná oprávnění pro přístup k souborům a portům, které používáte.
- Pro testování můžete použít `socat` ve spojení s dalšími nástroji, jako je `netcat`, pro snadné ověření připojení a přenosu dat.