# [Český] Debian Almquist Shell (dash) set: Nastavení shellových proměnných a vlastností

## Přehled
Příkaz `set` v shellu dash slouží k nastavení různých shellových proměnných a vlastností. Umožňuje uživatelům konfigurovat chování shellu a manipulovat s proměnnými prostředí.

## Použití
Základní syntaxe příkazu `set` je následující:

```
set [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Ukončí skript při jakékoliv chybě.
- `-u`: Ukončí skript, pokud se pokusíte použít neexistující proměnnou.
- `-x`: Zobrazí příkazy a jejich argumenty při jejich vykonávání, což je užitečné pro ladění.
- `-o`: Umožňuje nastavit různé vlastnosti shellu, jako například `-o noclobber`, což zabraňuje přepsání existujících souborů při přesměrování.

## Běžné příklady
### 1. Ukončení skriptu při chybě
```sh
set -e
# Příkaz, který může selhat
cp soubor.txt /neexistujici_cesta/
echo "Tento text se nezobrazí, pokud dojde k chybě."
```

### 2. Zobrazování příkazů pro ladění
```sh
set -x
echo "Toto je ladicí výstup."
set +x
```

### 3. Použití s proměnnými
```sh
set -u
echo $NEEXISTUJICI_PROMENNA
# Skript se ukončí s chybou, protože proměnná neexistuje.
```

### 4. Nastavení vlastnosti noclobber
```sh
set -o noclobber
echo "Nějaký text" > soubor.txt
echo "Nějaký text" > soubor.txt # Tato akce selže, pokud soubor již existuje.
```

## Tipy
- Používejte `set -e` pro zvýšení robustnosti skriptů, aby se automaticky ukončily při chybách.
- Kombinujte `set -u` s inicializací proměnných, abyste se vyhnuli chybám způsobeným neexistujícími proměnnými.
- Pro ladění skriptů je užitečné používat `set -x`, abyste viděli, jaké příkazy se vykonávají.