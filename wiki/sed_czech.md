# [Český] Debian Almquist Shell (dash) sed Použití: Úprava textových dat

## Přehled
Příkaz `sed` (stream editor) slouží k úpravě textových dat v reálném čase. Umožňuje provádět různé operace, jako je nahrazování, mazání nebo vkládání textu v souborech nebo na standardním vstupu.

## Použití
Základní syntaxe příkazu `sed` je následující:

```bash
sed [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Umožňuje specifikovat více příkazů `sed`.
- `-i`: Provádí úpravy přímo v souboru (in-place).
- `-n`: Potlačuje automatický výstup, což umožňuje použít příkaz `p` pro explicitní tisk.
- `s/patře/nový_text/`: Nahrazuje první výskyt `patře` s `nový_text`.

## Běžné příklady

### Nahrazení textu
Nahrazení slova "starý" slovem "nový" v souboru `soubor.txt`:

```bash
sed 's/starý/nový/' soubor.txt
```

### Nahrazení všech výskytů
Nahrazení všech výskytů slova "chyba" slovem "oprava":

```bash
sed 's/chyba/oprava/g' soubor.txt
```

### Odstranění řádků
Odstranění řádků, které obsahují slovo "nepotřebný":

```bash
sed '/nepotřebný/d' soubor.txt
```

### Vložení textu
Vložení textu "Nový řádek" před druhý řádek:

```bash
sed '2i Nový řádek' soubor.txt
```

### Uložení změn do souboru
Provádění změn přímo v souboru `soubor.txt`:

```bash
sed -i 's/starý/nový/g' soubor.txt
```

## Tipy
- Před použitím možnosti `-i` si vždy udělejte zálohu souboru, abyste předešli ztrátě dat.
- Používejte možnost `-n` spolu s příkazem `p`, pokud chcete vytisknout pouze specifické řádky.
- Experimentujte s různými regulárními výrazy pro pokročilejší úpravy textu.