# [Český] Debian Almquist Shell (dash) cal <Použití: zobrazení kalendáře>

## Přehled
Příkaz `cal` slouží k zobrazení kalendáře v terminálu. Umožňuje uživatelům rychle a snadno prohlížet měsíční nebo roční kalendáře přímo z příkazové řádky.

## Použití
Základní syntaxe příkazu je následující:

```
cal [možnosti] [argumenty]
```

## Běžné možnosti
- `-m`: Zobrazí kalendář s aktuálním měsícem zvýrazněným.
- `-y`: Zobrazí kalendář pro celý aktuální rok.
- `-3`: Zobrazí kalendář pro aktuální měsíc a měsíc před a po.
- `-j`: Zobrazí kalendář s dny v roce (Julian).
- `[měsíc] [rok]`: Umožňuje zobrazit kalendář pro specifikovaný měsíc a rok.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `cal`:

1. Zobrazení kalendáře pro aktuální měsíc:
   ```bash
   cal
   ```

2. Zobrazení kalendáře pro konkrétní měsíc a rok (např. červenec 2023):
   ```bash
   cal 07 2023
   ```

3. Zobrazení kalendáře pro celý aktuální rok:
   ```bash
   cal -y
   ```

4. Zobrazení kalendáře pro aktuální měsíc a měsíce před a po:
   ```bash
   cal -3
   ```

5. Zobrazení kalendáře s dny v roce:
   ```bash
   cal -j
   ```

## Tipy
- Používejte možnost `-m`, pokud chcete rychle zvýraznit aktuální měsíc.
- Pro plánování událostí může být užitečné zobrazit kalendář pro tři měsíce najednou pomocí `-3`.
- Pokud potřebujete zkontrolovat konkrétní datum, můžete snadno zadat měsíc a rok přímo do příkazu.