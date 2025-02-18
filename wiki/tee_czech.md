# [Český] Debian Almquist Shell (dash) tee použití: Zapisování výstupu do souboru a na standardní výstup

## Přehled
Příkaz `tee` slouží k čtení standardního vstupu a zapisování jeho obsahu jak na standardní výstup (obvykle terminál), tak do jednoho nebo více souborů. To je užitečné, když chcete vidět výstup příkazu a zároveň ho uložit pro pozdější použití.

## Použití
Základní syntaxe příkazu `tee` je následující:

```
tee [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`, `--append`: Přidá výstup na konec souboru místo jeho přepsání.
- `-i`, `--ignore-interrupts`: Ignoruje přerušení (např. Ctrl+C).
- `--help`: Zobrazí nápovědu k příkazu.
- `--version`: Zobrazí verzi příkazu.

## Běžné příklady
1. **Zapisování výstupu do souboru a na terminál:**
   ```bash
   echo "Ahoj světe" | tee soubor.txt
   ```

2. **Přidání výstupu na konec existujícího souboru:**
   ```bash
   echo "Další řádek" | tee -a soubor.txt
   ```

3. **Zapisování výstupu z příkazu do více souborů:**
   ```bash
   echo "Zapisování do více souborů" | tee soubor1.txt soubor2.txt
   ```

4. **Zobrazení výstupu a současné ukládání do souboru:**
   ```bash
   ls -l | tee seznam_souboru.txt
   ```

## Tipy
- Používejte možnost `-a`, pokud chcete přidávat data do existujících souborů, abyste neztratili předchozí obsah.
- Pokud pracujete s dlouhými příkazy, můžete použít `tee` k monitorování výstupu a zároveň ho ukládat pro pozdější analýzu.
- V kombinaci s dalšími příkazy (např. `grep`, `awk`) můžete efektivně filtrovat a ukládat specifické části výstupu.