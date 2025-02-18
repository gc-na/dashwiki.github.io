# [Debian] Debian Almquist Shell (dash) uniq használata: Ismétlődések eltávolítása

## Áttekintés
A `uniq` parancs a szövegfájlokban található ismétlődő sorokat távolítja el. Alapértelmezés szerint csak a szomszédos azonos sorokat kezeli, így a fájl rendezése gyakran szükséges a kívánt eredmény eléréséhez.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
uniq [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: Megszámolja az ismétlődő sorokat és azokat a sorok elé írja.
- `-d`: Csak azokat a sorokat jeleníti meg, amelyek többször is előfordulnak.
- `-u`: Csak azokat a sorokat mutatja, amelyek egyszer fordulnak elő.

## Gyakori példák
1. Ismétlődő sorok eltávolítása egy fájlból:
   ```bash
   uniq input.txt output.txt
   ```

2. Az ismétlődő sorok számának megjelenítése:
   ```bash
   uniq -c input.txt
   ```

3. Csak az ismétlődő sorok megjelenítése:
   ```bash
   uniq -d input.txt
   ```

4. Csak az egyedi sorok megjelenítése:
   ```bash
   uniq -u input.txt
   ```

## Tippek
- Használj `sort` parancsot a `uniq` előtt, ha biztosítani szeretnéd, hogy az ismétlődő sorok egymás mellett legyenek:
  ```bash
  sort input.txt | uniq
  ```
- Ha nagy fájlokkal dolgozol, érdemes a `-o` opciót használni az eredmény közvetlen fájlba írásához, elkerülve ezzel a memória túlterhelését.