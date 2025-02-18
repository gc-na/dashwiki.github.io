# [Český] Debian Almquist Shell (dash) tail použití: Zobrazí posledních několik řádků souboru

## Přehled
Příkaz `tail` slouží k zobrazení posledních několika řádků textového souboru. Je užitečný pro rychlé prohlížení obsahu souborů, zejména logů, kde je důležité vidět nejnovější záznamy.

## Použití
Základní syntaxe příkazu je následující:

```
tail [možnosti] [argumenty]
```

## Běžné možnosti
- `-n [číslo]`: Zobrazí posledních [číslo] řádků souboru.
- `-f`: Sleduje soubor v reálném čase a zobrazuje nové řádky, které jsou přidány.
- `-c [číslo]`: Zobrazí posledních [číslo] bajtů souboru.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `tail`:

1. Zobrazit posledních 10 řádků souboru `log.txt`:
   ```sh
   tail log.txt
   ```

2. Zobrazit posledních 20 řádků souboru `data.txt`:
   ```sh
   tail -n 20 data.txt
   ```

3. Sledovat soubor `access.log` v reálném čase:
   ```sh
   tail -f access.log
   ```

4. Zobrazit posledních 100 bajtů souboru `output.txt`:
   ```sh
   tail -c 100 output.txt
   ```

## Tipy
- Používejte `tail -f` při sledování logů, abyste mohli okamžitě vidět nové záznamy, jakmile jsou přidány.
- Kombinujte `tail` s dalšími příkazy, jako je `grep`, pro filtrování výstupu. Například:
  ```sh
  tail -f log.txt | grep "chyba"
  ```
- Pokud potřebujete zobrazit více než 10 řádků, můžete použít `-n` s požadovaným číslem, abyste přizpůsobili výstup svým potřebám.