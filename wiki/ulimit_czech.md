# [Český] Debian Almquist Shell (dash) ulimit: Omezování systémových prostředků

## Přehled
Příkaz `ulimit` slouží k nastavení nebo zobrazení limitů systémových prostředků, které mohou být použity procesy běžícími v shellu. Tyto limity pomáhají chránit systém před nadměrným využíváním prostředků.

## Použití
Základní syntaxe příkazu `ulimit` je následující:

```bash
ulimit [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny aktuální limity.
- `-c [velikost]`: Nastaví limit velikosti core souboru.
- `-d [velikost]`: Nastaví limit velikosti datového segmentu.
- `-f [velikost]`: Nastaví limit velikosti souboru.
- `-l [velikost]`: Nastaví limit velikosti zamknuté paměti.
- `-m [velikost]`: Nastaví limit velikosti fyzické paměti.
- `-n [počet]`: Nastaví limit počtu otevřených souborů.
- `-s [velikost]`: Nastaví limit velikosti zásobníku.
- `-t [čas]`: Nastaví limit CPU času v sekundách.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ulimit`:

1. Zobrazení všech aktuálních limitů:
   ```bash
   ulimit -a
   ```

2. Nastavení limitu velikosti souboru na 100 MB:
   ```bash
   ulimit -f 102400
   ```

3. Nastavení limitu počtu otevřených souborů na 200:
   ```bash
   ulimit -n 200
   ```

4. Zobrazení limitu pro velikost core souboru:
   ```bash
   ulimit -c
   ```

5. Nastavení limitu velikosti zásobníku na 8 MB:
   ```bash
   ulimit -s 8192
   ```

## Tipy
- Při nastavování limitů buďte opatrní, abyste nezabránili důležitým procesům v jejich správném fungování.
- Limity nastavené pomocí `ulimit` platí pouze pro aktuální shell a jeho podřízené procesy. Pokud potřebujete trvalé změny, upravte konfigurační soubory jako `/etc/security/limits.conf`.
- Používejte `ulimit -a` pro rychlou kontrolu aktuálních limitů před provedením změn.