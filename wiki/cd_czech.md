# [Český] Debian Almquist Shell (dash) cd použití: Přechod mezi adresáři

## Přehled
Příkaz `cd` (change directory) slouží k přechodu mezi adresáři v systému souborů. Umožňuje uživatelům měnit aktuální pracovní adresář v shellu.

## Použití
Základní syntaxe příkazu `cd` je následující:

```bash
cd [možnosti] [argumenty]
```

## Běžné možnosti
- `-`: Přepne se na předchozí adresář.
- `..`: Přechod do nadřazeného adresáře.
- `~`: Přechod do domovského adresáře uživatele.

## Běžné příklady
1. Přechod do domovského adresáře:
   ```bash
   cd ~
   ```

2. Přechod do nadřazeného adresáře:
   ```bash
   cd ..
   ```

3. Přechod do specifického adresáře:
   ```bash
   cd /cesta/k/adresáři
   ```

4. Přepnutí na předchozí adresář:
   ```bash
   cd -
   ```

## Tipy
- Používejte `cd` s absolutními cestami pro přesné určení umístění.
- Pokud si nejste jisti aktuálním adresářem, použijte příkaz `pwd` (print working directory) k zobrazení aktuální cesty.
- Vytvářejte aliasy pro často používané adresáře pro rychlejší přístup.