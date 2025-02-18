# [Debian] Debian Almquist Shell (dash) at: Plánování úloh

## Přehled
Příkaz `at` slouží k plánování jednorázových úloh, které se mají vykonat v určitém čase. Umožňuje uživatelům spouštět příkazy nebo skripty v budoucnosti, což je užitečné pro automatizaci úloh.

## Použití
Základní syntaxe příkazu `at` je následující:

```
at [možnosti] [argumenty]
```

## Běžné možnosti
- `-f <soubor>`: Určuje soubor, který obsahuje příkazy k vykonání.
- `-m`: Odesílá e-mail po dokončení úlohy, i když nebyly žádné chyby.
- `-q <fronta>`: Určuje frontu, do které bude úloha zařazena (např. `a`, `b`, `c`).
- `-t <čas>`: Umožňuje specifikovat čas v formátu `YYYYMMDDHHMM`.

## Běžné příklady
1. Naplánování úlohy na 5 minut později:
   ```sh
   echo "echo 'Ahoj, svět!'" | at now + 5 minutes
   ```

2. Naplánování úlohy na konkrétní čas:
   ```sh
   echo "backup.sh" | at 14:00
   ```

3. Použití souboru pro příkazy:
   ```sh
   at -f script.sh now + 1 hour
   ```

4. Naplánování úlohy s e-mailem po dokončení:
   ```sh
   echo "cleanup.sh" | at -m now + 10 minutes
   ```

## Tipy
- Ujistěte se, že máte povolenou službu `atd`, aby příkazy mohly být vykonány.
- Můžete zobrazit naplánované úlohy pomocí příkazu `atq`.
- Pokud chcete zrušit naplánovanou úlohu, použijte `atrm <ID>`, kde `<ID>` je číslo úlohy z výstupu `atq`.