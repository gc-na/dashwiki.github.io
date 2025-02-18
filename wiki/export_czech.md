# [Český] Debian Almquist Shell (dash) export použití: Nastavení proměnných prostředí

## Přehled
Příkaz `export` se používá k nastavení proměnných prostředí v shellu. Když proměnnou exportujete, stává se dostupnou pro všechny podřízené procesy, což je užitečné pro předávání konfigurací a nastavení mezi různými skripty a aplikacemi.

## Použití
Základní syntaxe příkazu `export` je následující:

```sh
export [možnosti] [argumenty]
```

## Běžné možnosti
- `-n`: Zruší export proměnné, takže nebude dostupná pro podřízené procesy.
- `-p`: Vypíše všechny exportované proměnné prostředí.

## Běžné příklady
1. **Export jednoduché proměnné:**
   ```sh
   MY_VAR="Hello, World!"
   export MY_VAR
   ```

2. **Export proměnné a její hodnoty v jedné řádce:**
   ```sh
   export MY_VAR="Hello, World!"
   ```

3. **Zrušení exportu proměnné:**
   ```sh
   export -n MY_VAR
   ```

4. **Zobrazení všech exportovaných proměnných:**
   ```sh
   export -p
   ```

## Tipy
- Ujistěte se, že proměnné, které exportujete, mají smysluplné názvy, aby bylo jasné, k čemu slouží.
- Pokud potřebujete použít proměnné v několika skriptech, zvažte jejich export v souboru `.profile` nebo `.bashrc`, aby byly dostupné při každém spuštění shellu.
- Při exportu citlivých informací, jako jsou hesla, buďte opatrní, aby nedošlo k jejich neúmyslnému zobrazení nebo úniku.