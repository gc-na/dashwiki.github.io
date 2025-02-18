# [Český] Debian Almquist Shell (dash) xargs použití: Zpracování standardního vstupu na argumenty příkazů

## Přehled
Příkaz `xargs` slouží k převodu vstupu ze standardního vstupu (např. z příkazu nebo souboru) na argumenty pro jiný příkaz. Umožňuje efektivně zpracovávat velké množství dat a předávat je dalším příkazům.

## Použití
Základní syntaxe příkazu `xargs` je následující:

```bash
xargs [možnosti] [argumenty]
```

## Běžné možnosti
- `-n N` – Určuje maximální počet argumentů, které budou předány jednomu příkazu.
- `-d DELIM` – Určuje oddělovač, který se použije pro rozdělení vstupu.
- `-0` – Očekává, že vstup bude ukončen nulovým znakem (užitečné při práci se soubory s mezerami v názvech).
- `-p` – Před každým provedením příkazu se dotáže uživatele na potvrzení.

## Běžné příklady
1. **Základní použití s `echo`:**
   ```bash
   echo "jablko banán hruška" | xargs mkdir
   ```
   Tento příkaz vytvoří adresáře `jablko`, `banán` a `hruška`.

2. **Použití s `find`:**
   ```bash
   find . -name "*.txt" | xargs rm
   ```
   Tento příkaz najde všechny soubory s příponou `.txt` a odstraní je.

3. **Použití s oddělovačem:**
   ```bash
   echo -e "jablko\nbanán\nhruška" | xargs -d '\n' echo
   ```
   Tento příkaz vytiskne `jablko`, `banán` a `hruška` na stejném řádku.

4. **Omezení počtu argumentů:**
   ```bash
   echo "soubor1 soubor2 soubor3 soubor4" | xargs -n 2 cp -t /cíl/
   ```
   Tento příkaz zkopíruje soubory po dvou do cílového adresáře.

## Tipy
- Používejte `-0` s příkazem `find` a `-print0`, abyste se vyhnuli problémům s mezerami v názvech souborů.
- Zvažte použití `-p`, pokud si nejste jisti, co příkaz udělá, abyste se vyhnuli nechtěným změnám.
- Při práci s velkým množstvím dat můžete použít `-n` pro optimalizaci výkonu a snížení zátěže systému.