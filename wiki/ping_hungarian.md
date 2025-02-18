# [Debian] Debian Almquist Shell (dash) ping használata: Hálózati elérhetőség ellenőrzése

## Overview
A `ping` parancs egy hálózati eszköz, amely lehetővé teszi a felhasználók számára, hogy ellenőrizzék egy másik számítógép elérhetőségét az interneten vagy egy helyi hálózaton. A parancs ICMP (Internet Control Message Protocol) echo kéréseket küld a megadott címre, és visszaigazolást vár a válaszokkal.

## Usage
A `ping` parancs alapvető szintaxisa a következő:

```bash
ping [opciók] [cím]
```

## Common Options
- `-c [szám]`: Megadja, hogy hány ping kérést küldjön a parancs.
- `-i [másodperc]`: Beállítja a ping kérések közötti várakozási időt másodpercben.
- `-s [méret]`: Meghatározza a küldött ICMP csomag méretét bájtban.
- `-t`: A ping kérések folytatása, amíg a felhasználó le nem állítja a parancsot.

## Common Examples
1. Alap ping egy címre:
   ```bash
   ping google.com
   ```

2. 5 ping kérés küldése:
   ```bash
   ping -c 5 google.com
   ```

3. Ping kérések küldése 2 másodperces intervallummal:
   ```bash
   ping -i 2 google.com
   ```

4. Ping kérések küldése 100 bájtos csomagokkal:
   ```bash
   ping -s 100 google.com
   ```

5. Ping folytatása, amíg le nem állítják:
   ```bash
   ping -t google.com
   ```

## Tips
- Használja a `-c` opciót, ha csak egy meghatározott számú ping kérést szeretne küldeni, hogy elkerülje a végtelen ciklusokat.
- Ellenőrizze a válaszidőt, hogy megtudja, mennyire gyorsan érkezik vissza a válasz a célcímről.
- Ha a ping parancs nem válaszol, ellenőrizze a hálózati kapcsolatot és a tűzfal beállításait.