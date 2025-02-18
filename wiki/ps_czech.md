# [Debian] Debian Almquist Shell (dash) ps použití: Zobrazení běžících procesů

## Přehled
Příkaz `ps` slouží k zobrazení aktuálně běžících procesů v systému. Umožňuje uživatelům sledovat, které procesy jsou aktivní, a poskytuje informace o jejich stavu, využití zdrojů a dalších parametrech.

## Použití
Základní syntaxe příkazu `ps` je následující:

```
ps [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Zobrazí všechny procesy.
- `-f`: Zobrazí procesy v úplném formátu, včetně informací o rodičovských procesech.
- `-u [uživatel]`: Zobrazí procesy patřící konkrétnímu uživateli.
- `-aux`: Zobrazí všechny procesy s podrobnými informacemi.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ps`:

### Zobrazení všech procesů
```bash
ps -e
```

### Zobrazení procesů s podrobnými informacemi
```bash
ps -aux
```

### Zobrazení procesů konkrétního uživatele
```bash
ps -u username
```

### Zobrazení procesů v úplném formátu
```bash
ps -ef
```

## Tipy
- Používejte kombinaci možností pro získání podrobnějších informací o procesech.
- Můžete použít příkaz `grep` k filtrování výstupu `ps`, například: 
  ```bash
  ps -e | grep nazev_procesu
  ```
- Zvažte použití příkazu `top` pro interaktivní sledování procesů v reálném čase.