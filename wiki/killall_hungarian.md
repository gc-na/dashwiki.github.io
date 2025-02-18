# [Debian] Debian Almquist Shell (dash) killall használata: Folyamatok leállítása név alapján

## Overview
A `killall` parancs lehetővé teszi a felhasználók számára, hogy egy adott nevű folyamatot leállítsanak a rendszerükön. Ez különösen hasznos, ha több példány fut egy adott programból, és mindet egyszerre szeretnénk megszüntetni.

## Usage
A `killall` parancs alapvető szintaxisa a következő:

```bash
killall [opciók] [argumentumok]
```

## Common Options
- `-u <felhasználónév>`: Csak a megadott felhasználó által indított folyamatokat állítja le.
- `-s <jelet>`: Meghatározza a jelet, amelyet a folyamatnak küldeni kell (például `SIGTERM` vagy `SIGKILL`).
- `-q`: Csendes mód, nem ír ki hibaüzeneteket, ha a folyamat nem található.
- `-n`: Csak a legújabb példányokat állítja le.

## Common Examples
- Minden példány leállítása a `firefox` programból:

```bash
killall firefox
```

- Csak a `gedit` program leállítása a saját felhasználói környezetből:

```bash
killall -u $(whoami) gedit
```

- A `myprocess` nevű folyamat leállítása, és a `SIGKILL` jel küldése:

```bash
killall -s SIGKILL myprocess
```

- Csendes mód használata, ha a `myapp` folyamat nem található:

```bash
killall -q myapp
```

## Tips
- Mindig ellenőrizd, hogy a megfelelő folyamatot állítod-e le, mivel a `killall` parancs minden példányt leállít a megadott név alapján.
- Használj `ps` vagy `pgrep` parancsokat a folyamatok listázására, mielőtt a `killall`-t használnád, hogy elkerüld a véletlen leállítást.
- A `killall` parancs használata előtt érdemes lehet menteni a folyamatok állapotát, ha azok adatokat kezelnek.