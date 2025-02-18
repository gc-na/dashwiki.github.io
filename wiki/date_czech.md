# [Český] Debian Almquist Shell (dash) příkaz date: [získání aktuálního data a času]

## Přehled
Příkaz `date` se používá k zobrazení a formátování aktuálního data a času v systému. Umožňuje uživatelům přizpůsobit výstup podle jejich potřeb.

## Použití
Základní syntaxe příkazu je následující:

```
date [možnosti] [argumenty]
```

## Běžné možnosti
- `+FORMAT` - Umožňuje specifikovat formát výstupu data a času.
- `-u` - Zobrazí čas v koordinovaném světovém čase (UTC).
- `-d "STRING"` - Zobrazí datum a čas, které odpovídají zadanému řetězci.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `date`:

1. Zobrazení aktuálního data a času:
   ```sh
   date
   ```

2. Zobrazení data ve formátu "den měsíc rok":
   ```sh
   date "+%d %m %Y"
   ```

3. Zobrazení aktuálního času v UTC:
   ```sh
   date -u
   ```

4. Zobrazení data a času pro specifikovaný řetězec:
   ```sh
   date -d "next Friday"
   ```

5. Zobrazení data a času v jiném formátu:
   ```sh
   date "+%Y-%m-%d %H:%M:%S"
   ```

## Tipy
- Používejte formátovací řetězce pro přizpůsobení výstupu podle svých potřeb.
- Pro zobrazení časových zón můžete použít příkaz `TZ` před příkazem `date`, například:
  ```sh
  TZ="America/New_York" date
  ```
- Experimentujte s různými formáty, abyste získali výstup, který nejlépe vyhovuje vašim požadavkům.