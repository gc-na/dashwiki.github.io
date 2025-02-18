# [Český] Debian Almquist Shell (dash) strace použití: Sledování systémových volání

## Přehled
Příkaz `strace` slouží k sledování systémových volání a signálů, které proces provádí. Umožňuje uživatelům diagnostikovat problémy s aplikacemi a pochopit, jak interagují se systémem.

## Použití
Základní syntaxe příkazu je následující:

```
strace [možnosti] [argumenty]
```

## Běžné možnosti
- `-e trace=SYSCALL`: Sledovat pouze specifikované systémové volání.
- `-o soubor`: Uložit výstup do zvoleného souboru místo na standardní výstup.
- `-p PID`: Sledovat již běžící proces s daným PID.
- `-c`: Zobrazit statistiky o systémových voláních.

## Běžné příklady
Sledování jednoduchého příkazu, například `ls`:

```bash
strace ls
```

Uložení výstupu do souboru:

```bash
strace -o vystup.txt ls
```

Sledování běžícího procesu s PID 1234:

```bash
strace -p 1234
```

Sledování pouze specifických systémových volání, například `open`:

```bash
strace -e trace=open ls
```

Zobrazení statistik o systémových voláních:

```bash
strace -c ls
```

## Tipy
- Používejte `strace` v kombinaci s jinými příkazy pro detailní analýzu.
- V případě sledování dlouhých procesů, jako jsou servery, zvažte použití `-o` pro uložení výstupu do souboru, abyste se vyhnuli zahlcení terminálu.
- Při sledování procesů s vysokou aktivitou můžete použít `-e trace=all`, ale buďte opatrní, protože výstup může být velmi rozsáhlý.