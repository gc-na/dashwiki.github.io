# [Debian] Debian Almquist Shell (dash) ulimit használat: A rendszer erőforrásainak korlátozása

## Áttekintés
Az `ulimit` parancs a shell környezetben lehetővé teszi a felhasználók számára, hogy korlátozzák a folyamatok által használt erőforrásokat, mint például a memória, a fájlok száma vagy a CPU idő. Ez segít megakadályozni, hogy egyetlen folyamat túl sok erőforrást használjon, ami a rendszer stabilitását veszélyeztetheti.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
ulimit [opciók] [érvek]
```

## Gyakori opciók
- `-a`: Megjeleníti az összes jelenlegi korlátozást.
- `-c`: Beállítja a core dump fájl maximális méretét.
- `-d`: Beállítja a folyamat adat szegmensének maximális méretét.
- `-f`: Beállítja a maximális fájlméretet, amelyet a folyamat létrehozhat.
- `-l`: Beállítja a maximális méretet a zárolt memóriához.
- `-m`: Beállítja a maximális memória méretet.
- `-n`: Beállítja a maximális fájlok számát, amelyet a folyamat megnyithat.
- `-s`: Beállítja a maximális veremméretet.
- `-t`: Beállítja a maximális CPU időt másodpercekben.
- `-v`: Beállítja a maximális virtuális memória méretet.

## Gyakori példák
1. Az összes korlátozás megjelenítése:
   ```bash
   ulimit -a
   ```

2. A maximális fájlméret beállítása 100 MB-ra:
   ```bash
   ulimit -f 102400
   ```

3. A maximális nyitható fájlok számának beállítása 2048-ra:
   ```bash
   ulimit -n 2048
   ```

4. A maximális CPU idő beállítása 60 másodpercre:
   ```bash
   ulimit -t 60
   ```

## Tippek
- Mindig ellenőrizd a jelenlegi korlátozásokat az `ulimit -a` paranccsal, mielőtt módosítanád őket.
- Használj megfelelő értékeket, hogy elkerüld a rendszer instabilitását.
- A korlátozások módosítása csak a jelenlegi shell munkamenetre vonatkozik, új shell indításakor az alapértelmezett beállítások lépnek érvénybe.