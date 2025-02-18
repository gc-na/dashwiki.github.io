# [Debian] Debian Almquist Shell (dash) groups használata: csoportok megjelenítése

## Overview
A `groups` parancs megjeleníti a felhasználóhoz tartozó csoportokat. Hasznos eszköz a felhasználói jogosultságok és csoporttagságok ellenőrzésére.

## Usage
A `groups` parancs alapvető szintaxisa a következő:

```bash
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: Megjeleníti a parancs használatára vonatkozó súgót.
- `--version`: Megjeleníti a parancs verzióját.

## Common Examples

1. **A saját csoportok megjelenítése:**
   ```bash
   groups
   ```

2. **Egy adott felhasználó csoportjainak megjelenítése:**
   ```bash
   groups felhasználónév
   ```

3. **Csoportok megjelenítése egy másik felhasználó nevének megadásával:**
   ```bash
   groups user1
   ```

4. **Súgó megjelenítése:**
   ```bash
   groups --help
   ```

## Tips
- Használja a `groups` parancsot a felhasználói jogosultságok gyors ellenőrzésére, különösen ha új csoportokat hoz létre.
- Ellenőrizze a csoporttagságokat, ha problémák merülnek fel a fájlokhoz való hozzáféréssel.
- A `groups` parancs kimenete segíthet a rendszeradminisztrátoroknak a felhasználói fiókok kezelésében.