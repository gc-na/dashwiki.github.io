# [Český] Debian Almquist Shell (dash) grep použití: Hledání textu v souborech

## Přehled
Příkaz `grep` slouží k vyhledávání textových řetězců v souborech. Umožňuje uživatelům efektivně najít konkrétní vzory v textu, což je užitečné při analýze logů, skriptů a dalších textových dat.

## Použití
Základní syntaxe příkazu `grep` je následující:

```bash
grep [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Ignoruje velikost písmen při vyhledávání.
- `-v`: Zobrazuje řádky, které NEOBSAHUJÍ daný vzor.
- `-r`: Prohledává adresáře rekurzivně.
- `-n`: Zobrazuje číslo řádku, na kterém se vzor nachází.
- `-l`: Zobrazuje pouze názvy souborů, které obsahují daný vzor.

## Běžné příklady
1. Hledání konkrétního slova v souboru:
    ```bash
    grep "slovo" soubor.txt
    ```

2. Hledání slova bez ohledu na velikost písmen:
    ```bash
    grep -i "slovo" soubor.txt
    ```

3. Zobrazení řádků, které neobsahují daný vzor:
    ```bash
    grep -v "slovo" soubor.txt
    ```

4. Rekurzivní hledání ve všech souborech v adresáři:
    ```bash
    grep -r "slovo" /cesta/k/adresáři
    ```

5. Zobrazení čísel řádků s nalezeným vzorem:
    ```bash
    grep -n "slovo" soubor.txt
    ```

## Tipy
- Používejte `-i`, pokud si nejste jisti velikostí písmen ve vyhledávaném vzoru.
- Kombinujte `grep` s dalšími příkazy, jako je `|`, pro efektivnější zpracování dat.
- Uložte výsledky vyhledávání do souboru pomocí přesměrování `>`, například:
    ```bash
    grep "slovo" soubor.txt > vysledky.txt
    ```