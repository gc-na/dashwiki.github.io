# [Český] Debian Almquist Shell (dash) diff použití: Porovnání souborů

## Přehled
Příkaz `diff` slouží k porovnání dvou souborů a zobrazení rozdílů mezi nimi. Tento nástroj je užitečný pro vývojáře a administrátory, kteří potřebují zjistit, jaké změny byly provedeny v textových souborech.

## Použití
Základní syntaxe příkazu `diff` je následující:

```bash
diff [možnosti] [argumenty]
```

## Běžné možnosti
- `-u`: Zobrazí rozdíly ve formátu unifikovaného výstupu, což je čitelnější.
- `-i`: Ignoruje rozdíly v velikosti písmen.
- `-w`: Ignoruje rozdíly v bílých znacích.
- `-r`: Porovnává adresáře rekurzivně.

## Běžné příklady
1. Porovnání dvou souborů:
   ```bash
   diff soubor1.txt soubor2.txt
   ```

2. Použití unifikovaného formátu:
   ```bash
   diff -u soubor1.txt soubor2.txt
   ```

3. Ignorování velikosti písmen:
   ```bash
   diff -i soubor1.txt soubor2.txt
   ```

4. Porovnání dvou adresářů rekurzivně:
   ```bash
   diff -r adresar1/ adresar2/
   ```

## Tipy
- Při porovnávání velkých souborů nebo adresářů použijte možnost `-u` pro přehlednější výstup.
- Pokud chcete výstup uložit do souboru, můžete použít přesměrování:
  ```bash
  diff soubor1.txt soubor2.txt > rozdily.txt
  ```
- Před porovnáním souborů se ujistěte, že máte správná oprávnění pro čtení těchto souborů.