# [Český] Debian Almquist Shell (dash) trap použití: Zpracování signálů a ukončení skriptů

## Přehled
Příkaz `trap` v shellu dash slouží k zachycení signálů a provádění specifických akcí, když dojde k jejich přijetí. Tento příkaz je užitečný pro správu chování skriptů při nečekaných událostech, jako je ukončení skriptu nebo přijetí signálu.

## Použití
Základní syntaxe příkazu `trap` je následující:

```sh
trap [možnosti] [argumenty]
```

## Běžné možnosti
- `SIGNAL`: Název signálu, který chcete zachytit (např. `SIGINT`, `SIGTERM`).
- `COMMAND`: Příkaz, který se má provést, když je signál přijat.

## Běžné příklady
1. **Zachycení signálu SIGINT (Ctrl+C)**:
   Tento příklad ukazuje, jak zachytit signál SIGINT a provést příkaz pro vyčištění před ukončením skriptu.

   ```sh
   trap 'echo "Skript byl přerušen"; exit' SIGINT
   ```

2. **Zachycení signálu SIGTERM**:
   Tento příklad provede příkaz pro uložení dat, když je skript ukončen signálem SIGTERM.

   ```sh
   trap 'echo "Ukládám data..."; save_data' SIGTERM
   ```

3. **Zachycení více signálů**:
   Můžete zachytit více signálů a při jejich přijetí provést stejnou akci.

   ```sh
   trap 'echo "Skript byl přerušen"; exit' SIGINT SIGTERM
   ```

## Tipy
- Používejte `trap` na začátku skriptu, abyste zajistili, že signály budou správně zachyceny.
- Zvažte použití `trap` pro úklidové úkoly, jako je odstranění dočasných souborů, když skript skončí.
- Testujte skript s různými signály, abyste se ujistili, že se chová podle očekávání.