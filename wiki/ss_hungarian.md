# [Debian] Debian Almquist Shell (dash) ss használata: Hálózati kapcsolatok megjelenítése

## Áttekintés
Az `ss` parancs a hálózati kapcsolatok és socketek állapotának megjelenítésére szolgál. Gyors és hatékony eszköz a rendszer hálózati teljesítményének ellenőrzésére.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
ss [opciók] [argumentumok]
```

## Gyakori opciók
- `-t`: Csak TCP kapcsolatok megjelenítése.
- `-u`: Csak UDP kapcsolatok megjelenítése.
- `-l`: Csak a hallgató socketek listázása.
- `-p`: A kapcsolatokhoz tartozó folyamatok megjelenítése.
- `-n`: A címek és portok numerikus formátumban való megjelenítése.

## Gyakori példák
1. **Összes kapcsolat megjelenítése**:
   ```bash
   ss
   ```

2. **Csak TCP kapcsolatok listázása**:
   ```bash
   ss -t
   ```

3. **Hallgató socketek megjelenítése**:
   ```bash
   ss -l
   ```

4. **UDP kapcsolatok megjelenítése**:
   ```bash
   ss -u
   ```

5. **A kapcsolatokhoz tartozó folyamatok megjelenítése**:
   ```bash
   ss -p
   ```

6. **Numerikus címek és portok megjelenítése**:
   ```bash
   ss -n
   ```

## Tippek
- Használj kombinált opciókat a részletesebb információkért, például `ss -tunlp` a TCP és UDP kapcsolatok, valamint a folyamatok megjelenítéséhez.
- A `ss` parancs gyorsabb és hatékonyabb, mint a régebbi `netstat` parancs, ezért érdemes ezt használni a hálózati kapcsolatok ellenőrzésére.
- Rendszeresen ellenőrizd a hálózati kapcsolataidat, hogy észleld a gyanús tevékenységeket vagy a teljesítményproblémákat.