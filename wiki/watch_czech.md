# [Český] Debian Almquist Shell (dash) watch použití: Sledujte změny v příkazech

## Přehled
Příkaz `watch` slouží k pravidelnému spouštění zadaného příkazu a zobrazení jeho výstupu na obrazovce. To je užitečné pro sledování změn v reálném čase, například při monitorování systémových informací nebo souborů.

## Použití
Základní syntaxe příkazu `watch` je následující:

```
watch [možnosti] [argumenty]
```

## Běžné možnosti
- `-n, --interval`: Určuje interval (v sekundách), jak často se má příkaz spouštět. Výchozí hodnota je 2 sekundy.
- `-d, --differences`: Zvýrazňuje rozdíly mezi výstupy příkazů.
- `-t, --no-title`: Skryje hlavičku s informacemi o čase a příkazu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `watch`:

1. Sledování obsahu adresáře:
   ```bash
   watch ls -l
   ```

2. Monitorování využití paměti:
   ```bash
   watch free -h
   ```

3. Sledování změn v souboru:
   ```bash
   watch -d cat /var/log/syslog
   ```

4. Sledování procesu s vlastním intervalem:
   ```bash
   watch -n 5 ps aux
   ```

## Tipy
- Používejte `-d` pro snadné sledování změn, což vám pomůže rychle identifikovat, co se změnilo.
- Pokud potřebujete sledovat příkaz s delším výstupem, zvažte použití `less` nebo `more` pro lepší čitelnost.
- Nezapomeňte, že příkaz `watch` může být užitečný i pro skripty, kde chcete monitorovat výstup v reálném čase.