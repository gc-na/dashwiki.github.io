# [Český] Debian Almquist Shell (dash) hostname použití: Zobrazí nebo nastaví název hostitele

## Přehled
Příkaz `hostname` slouží k zobrazení nebo nastavení názvu hostitele systému. Název hostitele je identifikátor, který se používá k rozlišení počítače v síti.

## Použití
Základní syntaxe příkazu je následující:

```sh
hostname [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`, `--fqdn`: Zobrazí plně kvalifikovaný název domény (FQDN).
- `-i`, `--ip-address`: Zobrazí IP adresu hostitele.
- `-s`, `--short`: Zobrazí krátký název hostitele.
- `--help`: Zobrazí nápovědu k použití příkazu.
- `--version`: Zobrazí verzi příkazu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `hostname`:

1. Zobrazení aktuálního názvu hostitele:
   ```sh
   hostname
   ```

2. Zobrazení plně kvalifikovaného názvu domény:
   ```sh
   hostname -f
   ```

3. Zobrazení IP adresy hostitele:
   ```sh
   hostname -i
   ```

4. Zobrazení krátkého názvu hostitele:
   ```sh
   hostname -s
   ```

5. Nastavení nového názvu hostitele:
   ```sh
   sudo hostname novy-nazev
   ```

## Tipy
- Při nastavování názvu hostitele se ujistěte, že nový název je jedinečný v rámci vaší sítě.
- Změna názvu hostitele může vyžadovat restartování některých služeb nebo systému, aby se projevila.
- Pro trvalé změny názvu hostitele můžete upravit soubor `/etc/hostname`.