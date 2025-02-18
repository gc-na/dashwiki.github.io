# [Debian] Debian Almquist Shell (dash) expr használata: matematikai kifejezések kiértékelése

## Áttekintés
Az `expr` parancs a Debian Almquist Shell (dash) környezetben matematikai kifejezések kiértékelésére szolgál. Lehetővé teszi az aritmetikai műveletek, logikai műveletek és karakterláncok kezelését.

## Használat
A parancs alapvető szintaxisa a következő:

```sh
expr [opciók] [argumentumok]
```

## Gyakori opciók
- `+` : Összeadás
- `-` : Kivonás
- `*` : Szorzás
- `/` : Osztás
- `%` : Maradékos osztás
- `=` : Egyenlőség vizsgálata
- `!=` : Különbözőség vizsgálata
- `:` : Karakterlánc hossza

## Gyakori példák
1. **Összeadás:**
   ```sh
   expr 5 + 3
   ```
   Eredmény: `8`

2. **Kivonás:**
   ```sh
   expr 10 - 4
   ```
   Eredmény: `6`

3. **Szorzás:**
   ```sh
   expr 7 \* 6
   ```
   Eredmény: `42`

4. **Osztás:**
   ```sh
   expr 20 / 4
   ```
   Eredmény: `5`

5. **Karakterlánc hossza:**
   ```sh
   expr length "Hello"
   ```
   Eredmény: `5`

6. **Egyenlőség vizsgálata:**
   ```sh
   expr 5 = 5
   ```
   Eredmény: `1` (igaz)

## Tippek
- Mindig használj visszaperceket (`\`) a szorzás (`*`) előtt, hogy elkerüld a shell értelmezési hibáit.
- Használj zárójeleket a bonyolultabb kifejezésekben a műveletek sorrendjének biztosításához.
- Az `expr` parancs kimenete egész szám, így ha lebegőpontos számokra van szükséged, érdemes más eszközöket használni, mint például a `bc`.