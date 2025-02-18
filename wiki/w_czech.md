# [Český] Debian Almquist Shell (dash) w: Zobrazí aktivní uživatele a jejich činnost

## Přehled
Příkaz `w` v shellu zobrazuje seznam aktuálně přihlášených uživatelů a jejich aktivitu. Poskytuje informace o tom, kdo je přihlášen, jak dlouho jsou přihlášeni a co právě dělají.

## Použití
Základní syntaxe příkazu `w` je následující:

```
w [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Skryje hlavičku výstupu.
- `-s`: Zobrazí zjednodušený formát bez některých informací.
- `-u`: Zobrazí uživatelské jméno uživatelů.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `w`:

1. Základní použití pro zobrazení aktivních uživatelů:
   ```bash
   w
   ```

2. Zobrazení bez hlavičky:
   ```bash
   w -h
   ```

3. Zjednodušený výstup:
   ```bash
   w -s
   ```

4. Zobrazení uživatelských jmen:
   ```bash
   w -u
   ```

## Tipy
- Používejte `w` pravidelně pro sledování aktivity uživatelů na serveru.
- Kombinujte `w` s dalšími příkazy, jako je `grep`, pro filtrování specifických uživatelů.
- Zvažte použití `w` v skriptech pro automatizaci monitorování uživatelské aktivity.