# [Debian] Debian Almquist Shell (dash) traceroute6 használata: Hálózati útvonalak nyomozása IPv6-on

## Áttekintés
A `traceroute6` parancs az IPv6 alapú hálózatokban használható, hogy megmutassa, milyen útvonalon haladnak a csomagok egy adott célállomás felé. A parancs segít a hálózati problémák diagnosztizálásában, mivel megjeleníti az egyes ugrások (hálózati eszközök) IP-címét és a válaszidőket.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
traceroute6 [opciók] [cél]
```

## Gyakori Opciók
- `-m <max_hop>`: Beállítja a maximális ugrások számát.
- `-p <port>`: Megadja a portszámot, amelyet a traceroute használ.
- `-w <másodperc>`: Beállítja a várakozási időt válaszként.
- `-n`: Az IP-címek numerikus formátumban való megjelenítése, névfeloldás nélkül.

## Gyakori Példák
1. Alap traceroute6 parancs egy IPv6 címre:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Maximális ugrások számának beállítása 15-re:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Portszám megadása (pl. 80):
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. Válaszidő beállítása 2 másodpercre:
   ```bash
   traceroute6 -w 2 2001:db8::1
   ```

5. IP-címek numerikus megjelenítése:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

## Tippek
- Használj `-n` opciót, ha gyorsabb eredményeket szeretnél, mivel elkerülöd a névfeloldást.
- A `-m` opcióval korlátozhatod az ugrások számát, ami hasznos lehet, ha csak a közeli hálózati eszközöket szeretnéd látni.
- Figyelj a válaszidőkre, mivel ezek segíthetnek a hálózati késleltetések azonosításában.