# [Český] Debian Almquist Shell (dash) exit <Použití ekvivalentní v češtině>: Ukončení skriptu nebo shellu

## Přehled
Příkaz `exit` se používá k ukončení aktuálního shellu nebo skriptu. Můžete také specifikovat návratový kód, který může být použit pro signalizaci úspěchu nebo chyby.

## Použití
Základní syntaxe příkazu `exit` je následující:

```sh
exit [možnosti] [argumenty]
```

## Běžné možnosti
- `n`: Volitelný argument, který určuje návratový kód. Pokud není uveden, použije se návratový kód posledního provedeného příkazu.

## Běžné příklady
1. Ukončení skriptu s návratovým kódem 0 (úspěch):

    ```sh
    exit 0
    ```

2. Ukončení skriptu s návratovým kódem 1 (chyba):

    ```sh
    exit 1
    ```

3. Ukončení interaktivního shellu:

    ```sh
    exit
    ```

4. Ukončení skriptu a předání návratového kódu z předchozího příkazu:

    ```sh
    ls /neexistujici_soubor
    exit $?
    ```

## Tipy
- Používejte `exit` na konci skriptů, abyste jasně signalizovali, jak skript skončil.
- Vždy se snažte vracet smysluplné návratové kódy, aby bylo možné snadno diagnostikovat chyby.
- Pokud spouštíte skript v interaktivním shellu, buďte opatrní při použití `exit`, protože to ukončí celý shell.