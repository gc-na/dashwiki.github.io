# [Český] Debian Almquist Shell (dash) who: zobrazení přihlášených uživatelů

## Přehled
Příkaz `who` slouží k zobrazení seznamu uživatelů, kteří jsou aktuálně přihlášeni do systému. Tento příkaz poskytuje informace o uživatelských účtech, jako je jejich jméno, terminál, čas přihlášení a další relevantní údaje.

## Použití
Základní syntaxe příkazu `who` je následující:

```
who [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny dostupné informace o uživatelích.
- `-b`: Zobrazí čas posledního restartu systému.
- `-q`: Zobrazí pouze seznam přihlášených uživatelů a jejich počet.
- `--help`: Zobrazí nápovědu k příkazu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `who`:

1. Zobrazit seznam všech přihlášených uživatelů:
   ```bash
   who
   ```

2. Zobrazit všechny dostupné informace o uživatelích:
   ```bash
   who -a
   ```

3. Zobrazit čas posledního restartu systému:
   ```bash
   who -b
   ```

4. Zobrazit pouze seznam přihlášených uživatelů a jejich počet:
   ```bash
   who -q
   ```

## Tipy
- Používejte možnost `-a`, pokud potřebujete podrobné informace o uživatelích a jejich aktivitě.
- Příkaz `who` je užitečný pro správce systému, kteří chtějí sledovat, kdo je v systému přihlášen.
- Můžete kombinovat příkaz `who` s dalšími příkazy, jako je `grep`, pro filtrování výsledků podle specifických uživatelů. Například:
  ```bash
  who | grep "uživatelské_jméno"
  ```