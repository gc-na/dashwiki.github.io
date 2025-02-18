# [Český] Debian Almquist Shell (dash) scp použití: Přenos souborů mezi hostiteli

## Přehled
Příkaz `scp` (secure copy) slouží k bezpečnému přenosu souborů mezi různými hostiteli v síti. Využívá protokol SSH pro zajištění šifrovaného přenosu dat.

## Použití
Základní syntaxe příkazu je následující:

```
scp [možnosti] [argumenty]
```

## Běžné možnosti
- `-r`: Rekurzivní kopírování adresářů.
- `-P`: Určení portu pro SSH (velké "P", protože malé "p" se používá pro jiný účel).
- `-i`: Určení souboru s privátním klíčem pro autentizaci.
- `-v`: Zobrazí podrobné informace o procesu přenosu.

## Běžné příklady
1. **Kopírování souboru z místního počítače na vzdálený server:**
   ```bash
   scp /cesta/k/souboru.txt uživatel@server:/cesta/na/serveru/
   ```

2. **Kopírování souboru z vzdáleného serveru na místní počítač:**
   ```bash
   scp uživatel@server:/cesta/k/souboru.txt /cesta/na/místním/počítači/
   ```

3. **Rekurzivní kopírování celého adresáře:**
   ```bash
   scp -r /cesta/k/adresáři/ uživatel@server:/cesta/na/serveru/
   ```

4. **Kopírování souboru na jiný port:**
   ```bash
   scp -P 2222 /cesta/k/souboru.txt uživatel@server:/cesta/na/serveru/
   ```

## Tipy
- Při kopírování citlivých dat vždy používejte `scp`, abyste zajistili šifrování přenosu.
- Pokud často používáte `scp`, zvažte nastavení SSH klíčů pro usnadnění autentizace.
- V případě velkých souborů nebo adresářů můžete použít `-v` pro sledování pokroku a diagnostiku případných problémů.