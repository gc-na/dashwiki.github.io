# [Debian] Debian Almquist Shell (dash) env használata: környezeti változók kezelése

## Overview
Az `env` parancs lehetővé teszi a környezeti változók megjelenítését és kezelését a shell környezetben. Ezen kívül új környezetben futtathatunk parancsokat, anélkül hogy módosítanánk a jelenlegi környezetet.

## Usage
A parancs alapvető szintaxisa a következő:

```bash
env [options] [arguments]
```

## Common Options
- `-i`: Üres környezet létrehozása, amely nem tartalmazza a meglévő környezeti változókat.
- `-u VAR`: Egy adott környezeti változó eltávolítása a környezetből.
- `-0`: A kimenetet null karakterrel elválasztja, ami hasznos lehet a fájlnevek kezelésénél.

## Common Examples
1. **Környezeti változók megjelenítése:**
   ```bash
   env
   ```

2. **Egy környezeti változó értékének megjelenítése:**
   ```bash
   env | grep PATH
   ```

3. **Új környezet létrehozása egy parancs futtatásához:**
   ```bash
   env VAR1=value1 VAR2=value2 command
   ```

4. **Környezetből egy változó eltávolítása:**
   ```bash
   env -u VAR1 command
   ```

5. **Üres környezet létrehozása:**
   ```bash
   env -i command
   ```

## Tips
- Használj `env`-t a szkriptek elején, hogy biztosítsd a szükséges környezeti változók beállítását.
- Ellenőrizd a környezeti változókat a `env` parancs segítségével, mielőtt egy új parancsot futtatnál.
- Az `-i` opció különösen hasznos, ha tiszta környezetben szeretnél futtatni egy parancsot, elkerülve a nem kívánt hatásokat.