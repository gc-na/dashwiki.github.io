# [Český] Debian Almquist Shell (dash) touch použití: Vytváření a aktualizace časových razítek souborů

## Přehled
Příkaz `touch` se používá k vytváření nových prázdných souborů nebo k aktualizaci časových razítek existujících souborů. Pokud soubor neexistuje, `touch` ho vytvoří; pokud existuje, aktualizuje čas posledního přístupu a poslední modifikace.

## Použití
Základní syntaxe příkazu je následující:

```bash
touch [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Aktualizuje pouze čas posledního přístupu.
- `-m`: Aktualizuje pouze čas poslední modifikace.
- `-c`: Nevytváří nové soubory, pokud neexistují.
- `-d <datum>`: Nastaví čas na specifikované datum a čas.

## Běžné příklady
1. Vytvoření nového prázdného souboru:
   ```bash
   touch novy_soubor.txt
   ```

2. Aktualizace časového razítka existujícího souboru:
   ```bash
   touch existujici_soubor.txt
   ```

3. Aktualizace pouze času posledního přístupu:
   ```bash
   touch -a existujici_soubor.txt
   ```

4. Nastavení specifického data a času:
   ```bash
   touch -d "2023-10-01 12:00:00" existujici_soubor.txt
   ```

5. Použití možnosti `-c` pro zabránění vytvoření nového souboru:
   ```bash
   touch -c neexistujici_soubor.txt
   ```

## Tipy
- Používejte `-c`, pokud chcete být jisti, že se nevytvoří nové soubory, když pracujete s neexistujícími názvy.
- Kombinujte možnosti `-a` a `-m`, pokud potřebujete aktualizovat obě časová razítka současně.
- Pro hromadnou aktualizaci více souborů jednoduše zadejte jejich názvy za příkazem `touch`, například:
  ```bash
  touch soubor1.txt soubor2.txt soubor3.txt
  ```