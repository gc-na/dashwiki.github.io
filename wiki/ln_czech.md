# [Český] Debian Almquist Shell (dash) ln použití: Vytváření symbolických a pevných odkazů

## Přehled
Příkaz `ln` se používá k vytváření odkazů na soubory v systému. Může vytvářet jak pevné odkazy, tak symbolické odkazy (symlinky), což umožňuje efektivní správu souborů a jejich umístění.

## Použití
Základní syntaxe příkazu `ln` je následující:

```
ln [možnosti] [argumenty]
```

## Běžné možnosti
- `-s`: Vytvoří symbolický odkaz místo pevného odkazu.
- `-f`: Přepíše existující soubor bez dotazu.
- `-n`: Při přepisování odkazů nezmění existující cílový soubor.
- `-v`: Zobrazí podrobnosti o tom, co příkaz dělá.

## Běžné příklady
1. **Vytvoření pevného odkazu:**
   ```bash
   ln soubor.txt odkaz.txt
   ```

2. **Vytvoření symbolického odkazu:**
   ```bash
   ln -s /cesta/k/souboru.txt odkaz.txt
   ```

3. **Přepsání existujícího odkazu:**
   ```bash
   ln -sf /nová/cesta/k/souboru.txt odkaz.txt
   ```

4. **Vytvoření symbolického odkazu s podrobnostmi:**
   ```bash
   ln -sv /cesta/k/souboru.txt odkaz.txt
   ```

## Tipy
- Používejte symbolické odkazy, pokud chcete odkazovat na soubory, které se mohou měnit nebo přesouvat.
- Při práci s pevnými odkazy mějte na paměti, že nemohou odkazovat na soubory na jiných svazcích.
- Vždy zkontrolujte existenci cílového souboru před přepisováním odkazů, abyste se vyhnuli nechtěným ztrátám dat.