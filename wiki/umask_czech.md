# [Český] Debian Almquist Shell (dash) umask použití: Nastavení výchozích oprávnění souborů

## Přehled
Příkaz `umask` slouží k nastavení výchozí masky oprávnění pro nově vytvářené soubory a adresáře. Tato maska určuje, jaká oprávnění budou odebrána z výchozích oprávnění, která by jinak byla při vytváření souboru nebo adresáře nastavena.

## Použití
Základní syntaxe příkazu `umask` je následující:

```
umask [možnosti] [argumenty]
```

## Běžné možnosti
- `-S`: Zobrazí masku v symbolickém formátu.
- `-p`: Zobrazí aktuální umask pro shell a její hodnotu.

## Běžné příklady
1. Zobrazení aktuální umask:
   ```sh
   umask
   ```

2. Nastavení umask na 022, což znamená, že nově vytvořené soubory budou mít oprávnění 644 a adresáře 755:
   ```sh
   umask 022
   ```

3. Zobrazení umask v symbolickém formátu:
   ```sh
   umask -S
   ```

4. Nastavení umask na 007, což znamená, že nově vytvořené soubory a adresáře budou mít oprávnění pouze pro vlastníka a skupinu:
   ```sh
   umask 007
   ```

## Tipy
- Při nastavování umasku mějte na paměti, že nižší číslo znamená více oprávnění. Například umask 000 znamená, že všechny oprávnění jsou povolena.
- Umask můžete nastavit v souboru `.profile` nebo `.bashrc`, aby se použil při každém spuštění shellu.
- Před změnou umasku se ujistěte, že rozumíte důsledkům, protože to ovlivní oprávnění všech nově vytvářených souborů a adresářů.