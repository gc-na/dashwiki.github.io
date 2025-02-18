# [Český] Debian Almquist Shell (dash) rm Použití: Odstranění souborů a adresářů

## Přehled
Příkaz `rm` slouží k odstranění souborů a adresářů v systému. Je to mocný nástroj, který by měl být používán opatrně, protože odstraněné soubory nelze snadno obnovit.

## Použití
Základní syntaxe příkazu je následující:

```
rm [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Vynucené odstranění, ignoruje neexistující soubory a nezobrazuje žádné varování.
- `-i`: Interaktivní režim, před odstraněním každého souboru se zeptá na potvrzení.
- `-r`: Rekurzivní odstranění, použije se pro odstranění adresářů a jejich obsahu.
- `-v`: Verbózní režim, zobrazuje podrobnosti o odstraněných souborech.

## Běžné příklady
- Odstranění jednoho souboru:
    ```bash
    rm soubor.txt
    ```

- Odstranění více souborů:
    ```bash
    rm soubor1.txt soubor2.txt
    ```

- Odstranění adresáře a jeho obsahu:
    ```bash
    rm -r adresar/
    ```

- Vynucené odstranění souboru bez potvrzení:
    ```bash
    rm -f soubor.txt
    ```

- Interaktivní odstranění, které se ptá na potvrzení:
    ```bash
    rm -i soubor.txt
    ```

## Tipy
- Vždy si dvakrát zkontrolujte, které soubory odstraňujete, zejména při použití možnosti `-f`.
- Používejte možnost `-i`, pokud si nejste jisti, abyste předešli nechtěnému odstranění důležitých souborů.
- Zvažte použití příkazu `mv` pro přesun souborů do koše místo jejich trvalého odstranění, pokud je to možné.