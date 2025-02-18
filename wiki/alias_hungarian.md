# [Debian] Debian Almquist Shell (dash) alias használata: parancsok egyszerűsítése

## Overview
Az `alias` parancs lehetővé teszi, hogy rövid neveket hozzunk létre hosszabb parancsok számára, így egyszerűbbé téve a parancsok használatát a parancssorban.

## Usage
A `alias` parancs alapvető szintaxisa a következő:

```bash
alias [opciók] [név]='[parancs]'
```

## Common Options
- `-p`: Megjeleníti az összes jelenlegi alias-t.
- `-d`: Törli a megadott alias-t.

## Common Examples
1. **Egyszerű alias létrehozása**:
   ```bash
   alias ll='ls -la'
   ```
   Ezzel az alias-szal a `ll` parancs a `ls -la` parancsot fogja futtatni.

2. **Alias megjelenítése**:
   ```bash
   alias
   ```
   Ez a parancs megjeleníti az összes jelenlegi alias-t.

3. **Alias törlése**:
   ```bash
   unalias ll
   ```
   Ezzel a paranccsal eltávolítjuk az `ll` alias-t.

4. **Alias létrehozása argumentumokkal**:
   ```bash
   alias grep='grep --color=auto'
   ```
   Ez az alias a `grep` parancsot színes kimenettel futtatja.

## Tips
- Használj érthető neveket az alias-okhoz, hogy könnyen emlékezhess rájuk.
- Az aliasokat érdemes a `~/.bashrc` vagy `~/.dashrc` fájlba menteni, hogy indításkor automatikusan betöltődjenek.
- Ellenőrizd az alias-ok listáját rendszeresen, hogy elkerüld a felesleges vagy ütköző alias-okat.