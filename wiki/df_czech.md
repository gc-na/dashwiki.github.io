# [Český] Debian Almquist Shell (dash) df použití: Zobrazí informace o využití diskového prostoru

## Přehled
Příkaz `df` slouží k zobrazení informací o využití diskového prostoru na připojených souborových systémech. Umožňuje uživatelům rychle zjistit, kolik místa je k dispozici a kolik je již obsazeno.

## Použití
Základní syntaxe příkazu je následující:

```
df [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí velikosti v lidsky čitelném formátu (např. KB, MB, GB).
- `-T`: Zobrazí typ souborového systému.
- `-a`: Zobrazí všechny souborové systémy, včetně těch, které nejsou připojené.
- `-i`: Zobrazí informace o inodech místo diskového prostoru.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `df`:

1. Základní zobrazení využití diskového prostoru:
   ```bash
   df
   ```

2. Zobrazení využití diskového prostoru v lidsky čitelném formátu:
   ```bash
   df -h
   ```

3. Zobrazení typů souborových systémů:
   ```bash
   df -T
   ```

4. Zobrazení všech souborových systémů, včetně nepřipojených:
   ```bash
   df -a
   ```

5. Zobrazení informací o inodech:
   ```bash
   df -i
   ```

## Tipy
- Používejte možnost `-h`, abyste snadno porozuměli velikostem diskového prostoru.
- Pravidelně kontrolujte využití diskového prostoru, abyste předešli problémům s nedostatkem místa.
- Kombinujte možnosti, například `df -hT`, pro zobrazení lidsky čitelných velikostí a typů souborových systémů současně.