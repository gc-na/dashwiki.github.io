# [Český] Debian Almquist Shell (dash) lsof Použití: Zobrazování otevřených souborů a procesů

## Přehled
Příkaz `lsof` (list open files) slouží k zobrazení seznamu otevřených souborů a procesů, které je používají. Tento nástroj je užitečný pro diagnostiku problémů se soubory a sledování aktivit procesů v systému.

## Použití
Základní syntaxe příkazu `lsof` je následující:

```bash
lsof [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Kombinuje další možnosti (AND).
- `-c [název]`: Zobrazí pouze soubory otevřené procesy s daným názvem.
- `-u [uživatel]`: Zobrazí pouze soubory otevřené procesy daného uživatele.
- `-p [PID]`: Zobrazí pouze soubory otevřené procesem s daným PID.
- `+D [adresář]`: Zobrazí soubory otevřené v daném adresáři a jeho podadresářích.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `lsof`:

1. Zobrazit všechny otevřené soubory:
   ```bash
   lsof
   ```

2. Zobrazit otevřené soubory pro konkrétního uživatele:
   ```bash
   lsof -u username
   ```

3. Zobrazit otevřené soubory pro konkrétní proces podle PID:
   ```bash
   lsof -p 1234
   ```

4. Zobrazit soubory otevřené procesy s názvem "bash":
   ```bash
   lsof -c bash
   ```

5. Zobrazit všechny soubory otevřené v určitém adresáři:
   ```bash
   lsof +D /cesta/k/adresáři
   ```

## Tipy
- Používejte `lsof` s administrátorskými právy (např. pomocí `sudo`), abyste získali úplný seznam otevřených souborů, včetně těch, které patří jiným uživatelům.
- Můžete kombinovat více možností pro specifikaci výstupu, například `lsof -u username -c bash` pro zobrazení souborů otevřených uživatelským procesem bash.
- Pokud potřebujete sledovat změny v reálném čase, můžete použít příkaz `watch` společně s `lsof`, například `watch lsof`.