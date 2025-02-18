# [Český] Debian Almquist Shell (dash) basename použití: Získání názvu souboru bez cesty

## Přehled
Příkaz `basename` slouží k extrakci názvu souboru z celého cesty. Odstraní všechny předchozí adresáře a případně také příponu souboru, což usnadňuje práci se soubory v shellu.

## Použití
Základní syntaxe příkazu je následující:

```
basename [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zpracovává více argumentů a vrací názvy souborů pro každý z nich.
- `-s Suffix`: Odstraní z názvu souboru zadanou příponu.

## Běžné příklady
1. Získání názvu souboru z cesty:
   ```sh
   basename /cesta/k/souboru.txt
   ```
   Výstup: `souboru.txt`

2. Získání názvu souboru bez přípony:
   ```sh
   basename /cesta/k/souboru.txt .txt
   ```
   Výstup: `souboru`

3. Zpracování více souborů najednou:
   ```sh
   basename -a /cesta/k/souboru1.txt /cesta/k/souboru2.txt
   ```
   Výstup:
   ```
   souboru1.txt
   souboru2.txt
   ```

4. Odstranění přípony z více souborů:
   ```sh
   basename -a /cesta/k/souboru1.txt /cesta/k/souboru2.txt .txt
   ```
   Výstup:
   ```
   souboru1
   souboru2
   ```

## Tipy
- Vždy se ujistěte, že správně zadáváte příponu, pokud ji chcete odstranit, aby nedošlo k nechtěnému výsledku.
- Používejte `basename` v kombinaci s dalšími příkazy, jako je `find`, pro efektivní zpracování souborů.
- Můžete použít `basename` v skriptech pro automatizaci úloh, které vyžadují práci s názvy souborů.