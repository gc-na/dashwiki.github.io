# [Český] Debian Almquist Shell (dash) sort použití: Řazení řádků textových souborů

## Přehled
Příkaz `sort` slouží k seřazení řádků textových souborů. Může být použit k uspořádání dat podle abecedy nebo číselně, což usnadňuje analýzu a zpracování textových informací.

## Použití
Základní syntaxe příkazu je následující:

```bash
sort [možnosti] [argumenty]
```

## Běžné možnosti
- `-r`: Řadí v opačném pořadí (sestupně).
- `-n`: Řadí čísla podle jejich hodnoty.
- `-k`: Umožňuje specifikovat klíč pro řazení (např. sloupec).
- `-u`: Odstraní duplicitní řádky.
- `-o`: Uloží výstup do souboru.

## Běžné příklady
Seřazení souboru `data.txt` podle abecedy:

```bash
sort data.txt
```

Seřazení souboru `data.txt` v opačném pořadí:

```bash
sort -r data.txt
```

Seřazení čísel v souboru `numbers.txt`:

```bash
sort -n numbers.txt
```

Seřazení podle druhého sloupce v souboru `data.txt`:

```bash
sort -k2 data.txt
```

Seřazení a odstranění duplicitních řádků:

```bash
sort -u data.txt
```

Uložení seřazeného výstupu do nového souboru `sorted_data.txt`:

```bash
sort data.txt -o sorted_data.txt
```

## Tipy
- Při práci s velkými soubory můžete použít `-S` pro určení velikosti paměti, kterou `sort` může použít.
- Pokud potřebujete řadit podle více sloupců, můžete použít více klíčů s `-k`, například `-k1,1 -k2,2`.
- Pro zajištění správného řazení s diakritikou můžete použít `LC_COLLATE` pro nastavení lokálního prostředí.