# [Debian] Debian Almquist Shell (dash) socat használata: Hálózati kapcsolatok létrehozása

## Overview
A `socat` (Socket Cat) egy sokoldalú parancssori eszköz, amely lehetővé teszi különböző típusú hálózati kapcsolatok létrehozását és kezelését. Képes adatokat továbbítani különböző források között, például fájlok, socketek és más programok között.

## Usage
A `socat` parancs alapvető szintaxisa a következő:

```bash
socat [opciók] [argumentumok]
```

## Common Options
- `-u`: Beállítja a socketet "unidirectional" (egyirányú) módba.
- `-v`: Verbose (részletes) kimenetet biztosít, amely segít a hibakeresésben.
- `TCP:<cím>:<port>`: TCP kapcsolat létrehozása a megadott címre és portra.
- `UDP:<cím>:<port>`: UDP kapcsolat létrehozása a megadott címre és portra.
- `FILE:<fájl>`: Fájl olvasása vagy írása.

## Common Examples
1. **TCP kapcsolat létrehozása egy távoli szerverhez:**
   ```bash
   socat TCP:example.com:80 -
   ```

2. **Adatok továbbítása egy helyi fájl és egy TCP socket között:**
   ```bash
   socat FILE:/path/to/file TCP:example.com:80
   ```

3. **Hálózati port továbbítása egy másik portra:**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:localhost:5678
   ```

4. **UDP kapcsolat létrehozása:**
   ```bash
   socat UDP:example.com:1234 -
   ```

## Tips
- Mindig ellenőrizd a tűzfal beállításait, hogy a szükséges portok nyitva legyenek.
- Használj `-v` opciót a hibaelhárításhoz, hogy részletes információt kapj a kapcsolatról.
- Kísérletezz a különböző protokollokkal (TCP, UDP), hogy megtaláld a legjobban működőt a feladatodhoz.