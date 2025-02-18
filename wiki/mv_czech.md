# [Český] Debian Almquist Shell (dash) mv Použití: Přesun a přejmenování souborů

## Přehled
Příkaz `mv` slouží k přesouvání a přejmenovávání souborů a adresářů v systému. Umožňuje uživatelům snadno organizovat soubory a měnit jejich názvy.

## Použití
Základní syntaxe příkazu `mv` je následující:

```
mv [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Interaktivní režim, který se ptá na potvrzení před přepsáním existujícího souboru.
- `-u`: Přesune soubor pouze v případě, že je zdrojový soubor novější než cílový nebo pokud cílový soubor neexistuje.
- `-v`: Zobrazí podrobnosti o tom, co se při přesouvání děje.

## Běžné příklady
Přesun souboru do jiného adresáře:
```bash
mv soubor.txt /cesta/k/adresáři/
```

Přejmenování souboru:
```bash
mv starý_název.txt nový_název.txt
```

Přesun více souborů do cílového adresáře:
```bash
mv soubor1.txt soubor2.txt /cesta/k/adresáři/
```

Použití interaktivního režimu:
```bash
mv -i soubor.txt /cesta/k/adresáři/
```

## Tipy
- Před použitím příkazu `mv` se ujistěte, že máte správná oprávnění pro cílový adresář.
- Používejte možnost `-i`, abyste se vyhnuli neúmyslnému přepsání souborů.
- Pokud často přejmenováváte soubory, zvažte použití skriptů pro automatizaci procesu.