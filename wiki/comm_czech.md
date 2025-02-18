# [Český] Debian Almquist Shell (dash) comm příkaz: Porovnání dvou tříděných souborů

## Přehled
Příkaz `comm` slouží k porovnání dvou tříděných textových souborů a zobrazuje řádky, které se vyskytují v jednom nebo obou souborech. Tento příkaz je užitečný pro analýzu rozdílů mezi dvěma soubory.

## Použití
Základní syntaxe příkazu je následující:

```
comm [možnosti] [soubory]
```

## Běžné možnosti
- `-1`: Potlačí výstup řádků, které jsou pouze v prvním souboru.
- `-2`: Potlačí výstup řádků, které jsou pouze ve druhém souboru.
- `-3`: Potlačí výstup řádků, které jsou společné oběma souborům.
- `-i`: Ignoruje rozdíly mezi velkými a malými písmeny.

## Běžné příklady
Porovnání dvou souborů `soubor1.txt` a `soubor2.txt`:

```bash
comm soubor1.txt soubor2.txt
```

Zobrazení pouze řádků, které jsou v `soubor1.txt`:

```bash
comm -13 soubor1.txt soubor2.txt
```

Zobrazení pouze řádků, které jsou v `soubor2.txt`:

```bash
comm -12 soubor1.txt soubor2.txt
```

Zobrazení pouze společných řádků:

```bash
comm -23 soubor1.txt soubor2.txt
```

## Tipy
- Ujistěte se, že soubory, které porovnáváte, jsou seřazeny, jinak může `comm` vrátit neplatné výsledky.
- Používejte možnosti `-i`, pokud chcete ignorovat rozdíly v malých a velkých písmenech, což může být užitečné při porovnávání textových souborů.
- Pro lepší přehlednost můžete výsledky přesměrovat do nového souboru pomocí `>`.

Tento příkaz je efektivní nástroj pro rychlé porovnání textových dat a může být velmi užitečný v různých skriptech a automatizovaných procesech.