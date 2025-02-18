# [Český] Debian Almquist Shell (dash) uniq použití: Odstranění duplicitních řádků

## Přehled
Příkaz `uniq` se používá k odstranění duplicitních řádků ze souboru nebo standardního vstupu. Tento příkaz porovnává sousední řádky a zachovává pouze první výskyt každého unikátního řádku.

## Použití
Základní syntaxe příkazu je následující:

```bash
uniq [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Před každým unikátním řádkem zobrazí počet jeho výskytů.
- `-d`: Zobrazí pouze duplicitní řádky.
- `-u`: Zobrazí pouze unikátní řádky.
- `-i`: Ignoruje rozdíly mezi velkými a malými písmeny při porovnávání.

## Běžné příklady
1. Odstranění duplicitních řádků ze souboru:
   ```bash
   uniq soubor.txt
   ```

2. Zobrazení počtu výskytů každého unikátního řádku:
   ```bash
   uniq -c soubor.txt
   ```

3. Zobrazení pouze duplicitních řádků:
   ```bash
   uniq -d soubor.txt
   ```

4. Zobrazení pouze unikátních řádků:
   ```bash
   uniq -u soubor.txt
   ```

5. Ignorování rozdílů mezi velkými a malými písmeny:
   ```bash
   uniq -i soubor.txt
   ```

## Tipy
- Před použitím příkazu `uniq` je dobré seřadit soubor pomocí příkazu `sort`, aby byly všechny duplicitní řádky vedle sebe:
  ```bash
  sort soubor.txt | uniq
  ```
- Používejte možnost `-c`, pokud potřebujete mít přehled o tom, kolikrát se jednotlivé řádky v souboru vyskytují.
- Při práci s velkými soubory může být užitečné použít `uniq` v kombinaci s dalšími příkazy, jako je `grep`, pro filtrování specifických řádků.