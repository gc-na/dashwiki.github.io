# [Český] Debian Almquist Shell (dash) head použití: Zobrazí prvních několik řádků souboru

## Přehled
Příkaz `head` slouží k zobrazení prvních několika řádků textového souboru. Je užitečný pro rychlý náhled obsahu souboru, aniž byste museli procházet celý soubor.

## Použití
Základní syntaxe příkazu je následující:

```sh
head [možnosti] [argumenty]
```

## Běžné možnosti
- `-n [číslo]`: Určuje počet řádků, které se mají zobrazit. Výchozí hodnota je 10.
- `-q`: Potlačuje hlavičky souborů, pokud je uvedeno více souborů.
- `-v`: Zobrazuje hlavičky souborů i při zobrazení jednoho souboru.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `head`:

1. Zobrazit prvních 10 řádků souboru `soubor.txt`:
    ```sh
    head soubor.txt
    ```

2. Zobrazit prvních 5 řádků souboru `data.txt`:
    ```sh
    head -n 5 data.txt
    ```

3. Zobrazit prvních 15 řádků souboru `log.txt` a potlačit hlavičku:
    ```sh
    head -n 15 -q log.txt
    ```

4. Zobrazit prvních 10 řádků z více souborů:
    ```sh
    head soubor1.txt soubor2.txt
    ```

## Tipy
- Používejte `head` v kombinaci s dalšími příkazy, jako je `grep`, pro efektivní filtrování výsledků.
- Pokud potřebujete rychle zkontrolovat strukturu souboru, `head` je ideální volbou, protože vám ukáže, jaké informace soubor obsahuje na začátku.
- Při práci s velkými soubory může být `head` užitečný pro rychlé ověření, zda soubor obsahuje očekávané údaje.