# [Český] Debian Almquist Shell (dash) expr použití: [provádění aritmetických a logických operací]

## Přehled
Příkaz `expr` slouží k provádění aritmetických a logických operací v shellu. Umožňuje vyhodnocovat výrazy a vracet výsledky, což je užitečné při skriptování a automatizaci úloh.

## Použití
Základní syntaxe příkazu je následující:

```
expr [možnosti] [argumenty]
```

## Běžné možnosti
- `+` : Sčítání dvou čísel.
- `-` : Odečítání druhého čísla od prvního.
- `*` : Násobení dvou čísel.
- `/` : Dělení prvního čísla druhým.
- `%` : Zbytek po dělení prvního čísla druhým.
- `=` : Porovnání dvou hodnot na rovnost.
- `!=` : Porovnání dvou hodnot na nerovnost.

## Běžné příklady
1. **Sčítání dvou čísel:**
   ```sh
   expr 5 + 3
   ```
   Výstup: `8`

2. **Odečítání:**
   ```sh
   expr 10 - 4
   ```
   Výstup: `6`

3. **Násobení:**
   ```sh
   expr 7 \* 6
   ```
   Výstup: `42`

4. **Dělení:**
   ```sh
   expr 20 / 4
   ```
   Výstup: `5`

5. **Porovnání hodnot:**
   ```sh
   expr 5 = 5
   ```
   Výstup: `1` (pravda)

6. **Zbytek po dělení:**
   ```sh
   expr 10 % 3
   ```
   Výstup: `1`

## Tipy
- Při použití operátoru `*` je nutné použít zpětné lomítko (`\`) před ním, aby se předešlo jeho interpretaci jako znaku pro vícenásobné argumenty.
- Pro porovnání čísel použijte `-eq`, `-ne`, `-lt`, `-le`, `-gt`, a `-ge` v rámci podmínek v shell skriptech.
- `expr` je užitečný pro jednoduché výpočty, ale pro složitější operace zvažte použití jiných nástrojů, jako je `bc` nebo `awk`.