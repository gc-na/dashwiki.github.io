# [Debian] Debian Almquist Shell (dash) pgrep használata: folyamatok keresése név alapján

## Áttekintés
A `pgrep` parancs lehetővé teszi a felhasználók számára, hogy folyamatokat keressenek a nevük vagy más jellemzőik alapján. Ez a parancs hasznos lehet, ha szeretnénk megtudni, hogy egy adott program fut-e a rendszerünkön.

## Használat
A `pgrep` parancs alapvető szintaxisa a következő:

```bash
pgrep [opciók] [argumentumok]
```

## Gyakori opciók
- `-u`: Keresés egy adott felhasználó által indított folyamatok között.
- `-f`: A teljes parancssort figyelembe veszi a keresés során.
- `-l`: A folyamatok nevét is megjeleníti a PID mellett.
- `-n`: Csak a legújabb folyamatot adja vissza.
- `-o`: Csak a legrégebbi folyamatot adja vissza.

## Gyakori példák
1. **Folyamat keresése név alapján**:
   ```bash
   pgrep firefox
   ```
   Ez a parancs visszaadja a `firefox` nevű folyamat PID-jét.

2. **Folyamatok keresése egy adott felhasználó által**:
   ```bash
   pgrep -u username
   ```
   Ezzel a paranccsal az `username` által indított folyamatok PID-jeit kaphatjuk meg.

3. **Teljes parancssor alapján történő keresés**:
   ```bash
   pgrep -f "python script.py"
   ```
   Ez a parancs a `python script.py` parancsot futtató folyamat PID-jét keresi.

4. **Folyamatok listázása PID és név szerint**:
   ```bash
   pgrep -l ssh
   ```
   Ez a parancs megjeleníti az `ssh` folyamatok PID-jét és nevét.

5. **Csak a legújabb folyamat keresése**:
   ```bash
   pgrep -n bash
   ```
   Ezzel a paranccsal a legújabb `bash` folyamat PID-jét kapjuk meg.

## Tippek
- Használja a `-l` opciót, ha szeretné látni a folyamat nevét a PID mellett, így könnyebben azonosíthatja a folyamatokat.
- A `-f` opcióval a teljes parancssor alapján is kereshet, ami hasznos lehet, ha a folyamat neve nem egyértelmű.
- Érdemes a `pgrep` parancsot a `pkill` parancssal kombinálni, ha a folyamatok leállítására is szükség van.