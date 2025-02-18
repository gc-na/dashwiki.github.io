# [Debian] Debian Almquist Shell (dash) netstat használata: Hálózati kapcsolat információk megjelenítése

## Áttekintés
A `netstat` parancs a hálózati kapcsolatok, a routing táblák, a interfészek statisztikái és a protokollok állapotának megjelenítésére szolgál. Hasznos eszköz a hálózati problémák diagnosztizálásához és a rendszer hálózati teljesítményének figyelemmel kíséréséhez.

## Használat
A `netstat` parancs alapvető szintaxisa a következő:

```bash
netstat [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a`: Minden kapcsolat és hallgató port megjelenítése.
- `-n`: A címek és portok numerikus formátumban történő megjelenítése.
- `-t`: Csak a TCP kapcsolatok megjelenítése.
- `-u`: Csak az UDP kapcsolatok megjelenítése.
- `-l`: Csak a hallgató portok megjelenítése.

## Gyakori Példák
1. **Minden aktív kapcsolat megjelenítése:**
   ```bash
   netstat -a
   ```

2. **Csak a TCP kapcsolatok megjelenítése:**
   ```bash
   netstat -t
   ```

3. **Numerikus címek és portok megjelenítése:**
   ```bash
   netstat -n
   ```

4. **Hallgató portok listázása:**
   ```bash
   netstat -l
   ```

5. **TCP és UDP kapcsolatok együttes megjelenítése:**
   ```bash
   netstat -tu
   ```

## Tippek
- Használja a `-p` opciót, hogy lássa, melyik folyamat használja a kapcsolatokat.
- A `netstat` parancs kimenete nagy mennyiségű információt tartalmazhat, ezért érdemes a `grep` parancsot használni a szűréshez.
- A `watch` parancs segítségével folyamatosan figyelemmel kísérheti a hálózati kapcsolatok állapotát:
  ```bash
  watch netstat -tuln
  ```