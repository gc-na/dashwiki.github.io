# [Český] Debian Almquist Shell (dash) tr <Použití>: převod a nahrazování znaků

## Přehled
Příkaz `tr` slouží k převodu a nahrazování znaků v textovém vstupu. Umožňuje uživatelům snadno měnit znaky v textových řetězcích, což je užitečné při zpracování textových souborů nebo dat.

## Použití
Základní syntaxe příkazu `tr` je následující:

```bash
tr [možnosti] [argumenty]
```

## Běžné možnosti
- `-d`: Odstraní zadané znaky.
- `-s`: Slučuje opakující se znaky do jednoho.
- `-c`: Používá znaky, které nejsou v zadaném seznamu.
- `-t`: Umožňuje převod znaků na jiné znaky.

## Běžné příklady
1. **Převod malých písmen na velká:**
   ```bash
   echo "ahoj světe" | tr 'a-z' 'A-Z'
   ```
   Tento příkaz převede všechny malé písmena na velká.

2. **Odstranění určitého znaku:**
   ```bash
   echo "ahoj světe" | tr -d 'o'
   ```
   Tento příkaz odstraní všechny znaky 'o' z textu.

3. **Slučování opakujících se mezer:**
   ```bash
   echo "ahoj    světe" | tr -s ' '
   ```
   Tento příkaz zredukuje více mezer na jednu.

4. **Převod znaků pomocí tabulky:**
   ```bash
   echo "12345" | tr '123' 'abc'
   ```
   Tento příkaz nahradí čísla 1, 2 a 3 písmeny a, b a c.

## Tipy
- Při použití `tr` je dobré mít na paměti, že příkaz pracuje pouze s jednotlivými znaky, nikoli s řetězci.
- Můžete kombinovat více možností pro komplexnější úpravy textu.
- Příkaz `tr` je velmi efektivní pro zpracování dat v rourách (pipes), což umožňuje snadnou integraci s jinými příkazy.