# [Český] Debian Almquist Shell (dash) batch použití: Spouštění příkazů v dávkách

## Přehled
Příkaz `batch` slouží k plánování úloh, které se mají vykonat, když je systém méně vytížený. Umožňuje uživatelům zadávat příkazy, které budou vykonány později, obvykle v době, kdy je zatížení systému nízké.

## Použití
Základní syntaxe příkazu `batch` je následující:

```
batch [možnosti] [argumenty]
```

## Běžné možnosti
- `-f` : Umožňuje specifikovat soubor, který obsahuje příkazy k vykonání.
- `-q` : Spustí `batch` v tichém režimu, bez výstupu na obrazovku.

## Běžné příklady
1. **Zadání jednoduchého příkazu k vykonání:**
   ```bash
   echo "echo 'Hello, World!'" | batch
   ```

2. **Vykonání skriptu uloženého v souboru:**
   ```bash
   batch < myscript.sh
   ```

3. **Zadání více příkazů:**
   ```bash
   {
       echo "První příkaz"
       echo "Druhý příkaz"
   } | batch
   ```

4. **Použití s možností -f:**
   ```bash
   batch -f mycommands.txt
   ```

## Tipy
- Ujistěte se, že příkazy, které zadáváte, jsou správné a testované, protože se vykonají bez dalšího potvrzení.
- Používejte `batch` pro úlohy, které mohou trvat delší dobu a které nechcete spouštět během špičky.
- Můžete kombinovat `batch` s dalšími příkazy pro efektivnější plánování úloh.