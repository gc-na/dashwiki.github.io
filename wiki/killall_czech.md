# [Český] Debian Almquist Shell (dash) killall <Použití>: Ukončení procesů podle názvu

## Přehled
Příkaz `killall` slouží k ukončení všech procesů, které běží pod daným názvem. Je to užitečný nástroj pro správu procesů, když potřebujete rychle zastavit více instancí určitého programu.

## Použití
Základní syntaxe příkazu `killall` je následující:

```
killall [možnosti] [argumenty]
```

## Běžné možnosti
- `-q`: Potlačí chybové zprávy, pokud žádný proces není nalezen.
- `-v`: Zobrazí podrobné informace o tom, které procesy byly ukončeny.
- `-s SIGNAL`: Určuje signál, který má být odeslán procesům (např. `-s SIGKILL` pro okamžité ukončení).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `killall`:

1. Ukončení všech instancí programu `firefox`:
   ```bash
   killall firefox
   ```

2. Ukončení všech procesů `python`, s podrobným výstupem:
   ```bash
   killall -v python
   ```

3. Odeslání signálu SIGKILL na všechny procesy `gedit`:
   ```bash
   killall -s SIGKILL gedit
   ```

4. Potlačení chybových zpráv při ukončení procesů `myapp`, pokud žádný neběží:
   ```bash
   killall -q myapp
   ```

## Tipy
- Před použitím `killall` se ujistěte, že znáte názvy procesů, které chcete ukončit, abyste nezastavili něco důležitého.
- Používejte volbu `-v`, pokud chcete mít přehled o tom, které procesy byly úspěšně ukončeny.
- Pokud potřebujete ukončit procesy, které běží pod jiným uživatelským účtem, můžete potřebovat administrátorská práva (např. pomocí `sudo`).