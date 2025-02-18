# [Debian] Debian Almquist Shell (dash) nslookup használata: DNS lekérdezések végrehajtása

## Áttekintés
Az `nslookup` parancs egy hálózati eszköz, amely lehetővé teszi a Domain Name System (DNS) lekérdezések végrehajtását. Ezzel a paranccsal IP-címeket és domain neveket lehet lekérdezni, valamint információkat kaphatunk a DNS szerverekről.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
nslookup [opciók] [argumentumok]
```

## Gyakori opciók
- `-type=TYPE`: Meghatározza a lekérdezni kívánt rekord típusát (pl. A, MX, CNAME).
- `-timeout=TIME`: Beállítja a várakozási időt másodpercekben a DNS válaszra.
- `-retry=COUNT`: Megadja, hogy hány próbálkozást tegyen a DNS lekérdezés során.

## Gyakori példák
1. **IP-cím lekérdezése domain név alapján:**
   ```bash
   nslookup example.com
   ```

2. **Domain név lekérdezése IP-cím alapján:**
   ```bash
   nslookup 93.184.216.34
   ```

3. **MX rekordok lekérdezése:**
   ```bash
   nslookup -type=MX example.com
   ```

4. **Egyéni DNS szerver használata:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Tippek
- Használj `-type=ANY` opciót, ha az összes elérhető rekordot szeretnéd megtekinteni egy domain névhez.
- Ellenőrizd a DNS válaszokat különböző DNS szerverekkel, hogy megbizonyosodj a helyes működésről.
- Használj `-debug` opciót a részletes hibaüzenetek megjelenítéséhez, ha problémák merülnek fel a lekérdezés során.