# [Český] Debian Almquist Shell (dash) logout použití: Odhlášení z aktuální relace

## Přehled
Příkaz `logout` se používá k odhlášení uživatele z aktuální relace shellu. Tento příkaz je užitečný, když chcete ukončit relaci a vrátit se na přihlašovací obrazovku nebo zavřít terminál.

## Použití
Základní syntaxe příkazu je následující:

```
logout [options]
```

## Běžné možnosti
- **--help**: Zobrazí nápovědu k příkazu `logout`.
- **--version**: Zobrazí verzi shellu.

## Běžné příklady
1. **Základní odhlášení**:
   Chcete-li se odhlásit z aktuální relace, jednoduše zadejte:
   ```sh
   logout
   ```

2. **Zobrazení nápovědy**:
   Pokud potřebujete pomoc, můžete použít:
   ```sh
   logout --help
   ```

3. **Zobrazení verze**:
   Pro zjištění verze shellu použijte:
   ```sh
   logout --version
   ```

## Tipy
- Ujistěte se, že jste uložili všechny změny v souborech před odhlášením, abyste neztratili žádná data.
- Příkaz `logout` je obvykle dostupný pouze v interaktivních shellech, takže se ujistěte, že jej používáte v správném kontextu.