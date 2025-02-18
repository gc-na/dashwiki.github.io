# [Český] Debian Almquist Shell (dash) unzip použití: Rozbalení souborů ZIP

## Přehled
Příkaz `unzip` slouží k rozbalení souborů ve formátu ZIP. Umožňuje extrahovat soubory z archivu a pracovat s nimi na vašem systému.

## Použití
Základní syntaxe příkazu `unzip` je následující:

```sh
unzip [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí seznam souborů v archivu bez jejich rozbalení.
- `-d [adresář]`: Určuje cílový adresář, do kterého budou soubory rozbaleny.
- `-o`: Přepíše existující soubory bez dotazu.
- `-q`: Potlačí výstup, takže se zobrazí pouze chyby.

## Běžné příklady
1. Rozbalení souboru `soubor.zip` do aktuálního adresáře:
   ```sh
   unzip soubor.zip
   ```

2. Rozbalení souboru `soubor.zip` do specifického adresáře `cílový_adresář`:
   ```sh
   unzip soubor.zip -d cílový_adresář
   ```

3. Zobrazení obsahu archivu `soubor.zip` bez rozbalení:
   ```sh
   unzip -l soubor.zip
   ```

4. Rozbalení souboru a přepsání existujících souborů bez dotazu:
   ```sh
   unzip -o soubor.zip
   ```

## Tipy
- Pokud často pracujete s archivy, zvažte použití možnosti `-d` pro organizaci rozbalených souborů do specifických adresářů.
- Používejte možnost `-q`, pokud chcete minimalizovat výstup příkazu, například při skriptování.
- Před rozbalením si vždy zkontrolujte obsah archivu pomocí `-l`, abyste věděli, co očekávat.