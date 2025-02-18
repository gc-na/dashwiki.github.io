# [Český] Debian Almquist Shell (dash) cmp <Použití: Porovnání souborů>

## Přehled
Příkaz `cmp` slouží k porovnání dvou souborů a zjištění, zda jsou identické. Pokud se soubory liší, `cmp` také ukáže, na kterých bytech se rozdíly nacházejí.

## Použití
Základní syntaxe příkazu je následující:

```bash
cmp [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí rozdíly v hexadecimálním formátu.
- `-s`: Tichý režim; neprovádí žádný výstup, pouze vrací stavový kód.
- `-i OFFSET`: Porovnává soubory od zadaného offsetu.
- `-n N`: Porovnává pouze prvních N bajtů souborů.

## Běžné příklady
Porovnání dvou souborů:

```bash
cmp soubor1.txt soubor2.txt
```

Použití tichého režimu pro porovnání:

```bash
cmp -s soubor1.txt soubor2.txt
```

Zobrazení rozdílů v hexadecimálním formátu:

```bash
cmp -l soubor1.txt soubor2.txt
```

Porovnání pouze prvních 100 bajtů:

```bash
cmp -n 100 soubor1.txt soubor2.txt
```

## Tipy
- Používejte `-s`, pokud chcete rychle zjistit, zda jsou soubory identické, aniž byste potřebovali podrobnosti.
- Pokud často porovnáváte velké soubory, zvažte použití `-n` pro omezení počtu porovnávaných bajtů, což může urychlit proces.
- V případě, že potřebujete porovnat binární soubory, `cmp` je ideální volbou, protože dokáže pracovat s jakýmikoli typy souborů.