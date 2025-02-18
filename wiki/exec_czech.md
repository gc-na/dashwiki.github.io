# [Debian] Debian Almquist Shell (dash) exec použití: Spuštění příkazů v aktuálním shellu

## Přehled
Příkaz `exec` v shellu dash slouží k nahrazení aktuálního shell procesu jiným příkazem. To znamená, že když použijete `exec`, aktuální shell se ukončí a místo něj se spustí nový příkaz. Tento příkaz přebírá všechny vlastnosti a prostředí aktuálního shellu.

## Použití
Základní syntaxe příkazu `exec` je následující:

```sh
exec [možnosti] [argumenty]
```

## Běžné možnosti
- `-a` : Umožňuje specifikovat alternativní jméno pro příkaz.
- `-l` : Spustí příkaz jako login shell.
- `-p` : Umožňuje spouštět příkaz s privilegii.

## Běžné příklady
1. Nahrazení aktuálního shellu příkazem `bash`:
   ```sh
   exec bash
   ```

2. Spuštění skriptu `myscript.sh` a ukončení aktuálního shellu:
   ```sh
   exec ./myscript.sh
   ```

3. Spuštění příkazu `top` místo aktuálního shellu:
   ```sh
   exec top
   ```

4. Použití `-a` pro změnu názvu příkazu:
   ```sh
   exec -a novy_nazev /bin/ls
   ```

## Tipy
- Používejte `exec`, když chcete, aby se nový proces stal hlavním procesem bez návratu do původního shellu.
- Buďte opatrní při používání `exec`, protože ukončí aktuální shell a ztrácíte tak všechny neuložené změny.
- Pokud potřebujete spustit příkaz a vrátit se zpět do shellu, zvažte použití běžného příkazu bez `exec`.