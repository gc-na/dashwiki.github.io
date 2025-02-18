# [Český] Debian Almquist Shell (dash) xz: Komprese a dekomprese souborů

## Přehled
Příkaz `xz` slouží k efektivní kompresi a dekompresi souborů pomocí algoritmu LZMA. Je oblíbený pro svou vysokou kompresní účinnost a je často používán pro zmenšení velikosti souborů, což usnadňuje jejich přenos a ukládání.

## Použití
Základní syntaxe příkazu `xz` je následující:

```bash
xz [možnosti] [argumenty]
```

## Běžné možnosti
- `-d`, `--decompress`: Dekomprimuje soubor.
- `-k`, `--keep`: Zachová původní soubor po kompresi.
- `-f`, `--force`: Přepíše existující soubory bez potvrzení.
- `-9`: Použije maximální úroveň komprese (0-9).
- `-t`, `--test`: Ověří integritu komprimovaného souboru.

## Běžné příklady
Kompresní příkaz pro soubor:

```bash
xz soubor.txt
```

Dekomprese souboru:

```bash
xz -d soubor.txt.xz
```

Kompresní příkaz s uchováním původního souboru:

```bash
xz -k soubor.txt
```

Testování integrity komprimovaného souboru:

```bash
xz -t soubor.txt.xz
```

## Tipy
- Používejte `-9` pro maximální kompresi, pokud je důležitá velikost souboru.
- Vždy testujte komprimované soubory pomocí `-t`, abyste zajistili, že nedošlo k poškození dat.
- Zvažte použití `-k`, pokud potřebujete mít k dispozici jak původní, tak komprimovaný soubor.