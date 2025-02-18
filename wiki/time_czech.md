# [Český] Debian Almquist Shell (dash) time použití: měření doby trvání příkazů

## Přehled
Příkaz `time` se používá k měření doby trvání vykonávání jiného příkazu. Umožňuje uživatelům zjistit, jak dlouho trvá provedení specifikovaného příkazu, a poskytuje informace o využití procesoru a dalších zdrojích.

## Použití
Základní syntaxe příkazu `time` je následující:

```bash
time [možnosti] [argumenty]
```

## Běžné možnosti
- `-p`: Zobrazí výstup v jednoduchém formátu, který je snadno čitelný.
- `--verbose`: Zobrazí podrobnější informace o prováděném příkazu.
- `-o soubor`: Uloží výstup do zadaného souboru místo na standardní výstup.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `time`:

1. Měření doby trvání příkazu `sleep`:
   ```bash
   time sleep 2
   ```

2. Měření doby trvání kopírování souboru:
   ```bash
   time cp soubor.txt /cesta/k/cilovemu/souboru.txt
   ```

3. Uložení výstupu do souboru:
   ```bash
   time -o vysledky.txt ls -l
   ```

4. Použití s volbou pro jednoduchý výstup:
   ```bash
   time -p ls
   ```

## Tipy
- Používejte volbu `-o`, pokud chcete uchovat výsledky měření pro pozdější analýzu.
- Pro rychlé měření doby trvání příkazů v skriptech je `time` velmi užitečný.
- Nezapomeňte, že `time` měří pouze dobu trvání příkazu, nikoli jeho výstup.