# [Debian] Debian Almquist Shell (dash) hostname használata: A gép neve

## Áttekintés
A `hostname` parancs a rendszer aktuális gépnevének megjelenítésére és beállítására szolgál. Ez a név azonosítja a számítógépet a hálózaton, és fontos szerepet játszik a hálózati kommunikációban.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
hostname [opciók] [argumentumok]
```

## Gyakori Opciók
- `-f`, `--fqdn`: Megjeleníti a teljes, minősített gépnevet (FQDN).
- `-i`, `--ip-address`: Megjeleníti a gép IP-címét.
- `-s`, `--short`: Megjeleníti a rövid gépnevet.
- `--help`: Információt ad a parancs használatáról.

## Gyakori Példák
1. A jelenlegi gépnév megjelenítése:
   ```bash
   hostname
   ```

2. A teljes, minősített gépnév megjelenítése:
   ```bash
   hostname -f
   ```

3. A gép IP-címének megjelenítése:
   ```bash
   hostname -i
   ```

4. A rövid gépnév megjelenítése:
   ```bash
   hostname -s
   ```

5. A gépnév beállítása:
   ```bash
   sudo hostname új_gépnév
   ```

## Tippek
- A `hostname` parancs használata előtt érdemes ellenőrizni, hogy van-e elegendő jogosultságod a gépnév megváltoztatásához.
- A gépnév megváltoztatása után érdemes újraindítani a rendszert, hogy a változtatások érvénybe lépjenek.
- Használj ékezet nélküli, egyszerű karaktereket a gépnévben, hogy elkerüld a hálózati problémákat.