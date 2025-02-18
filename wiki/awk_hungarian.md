# [Debian] Debian Almquist Shell (dash) awk használata: Szövegfeldolgozás és mintakeresés

## Áttekintés
Az `awk` egy hatékony szövegfeldolgozó eszköz, amely lehetővé teszi a fájlok és adatok minták szerinti keresését és manipulálását. Az `awk` programozási nyelvként is funkcionál, amely segít a szöveges adatok elemzésében és formázásában.

## Használat
Az `awk` parancs alapvető szintaxisa a következő:

```bash
awk [opciók] [argumentumok]
```

## Gyakori opciók
- `-F`: Megadja a mezőelválasztót (pl. `-F,` a CSV fájlokhoz).
- `-v`: Változókat definiál, amelyeket az `awk` programban használhatunk.
- `-f`: Külső fájlban található `awk` programot futtat.

## Gyakori példák

1. **Egyszerű mezők kiírása**: Az alábbi példa kiírja az első mezőt egy fájlból.
   ```bash
   awk '{print $1}' fajl.txt
   ```

2. **Mezőelválasztó megadása**: CSV fájlok esetén a következő parancs használható.
   ```bash
   awk -F, '{print $2}' fajl.csv
   ```

3. **Feltételes kiírás**: Csak azokat a sorokat írja ki, ahol a második mező nagyobb, mint 100.
   ```bash
   awk '$2 > 100 {print}' fajl.txt
   ```

4. **Változó használata**: A következő példa egy változót definiál, amelyet a kimenetben használunk.
   ```bash
   awk -v val=10 '$1 > val {print $0}' fajl.txt
   ```

5. **Összegzés**: Az alábbi parancs összegzi az első mező értékeit.
   ```bash
   awk '{sum += $1} END {print sum}' fajl.txt
   ```

## Tippek
- Használj mezőelválasztókat a pontosabb adatelemzéshez.
- A `BEGIN` és `END` blokkok segítségével előkészítheted a környezetet és a kimenetet.
- Kísérletezz a változók használatával a bonyolultabb logika megvalósításához.