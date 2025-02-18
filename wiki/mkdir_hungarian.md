# [Debian] Debian Almquist Shell (dash) mkdir használata: Mappák létrehozása

## Áttekintés
A `mkdir` parancs a Debian Almquist Shell (dash) környezetben új mappák (könyvtárak) létrehozására szolgál. Ez a parancs lehetővé teszi a felhasználók számára, hogy könnyedén szervezhessék fájljaikat és mappáikat.

## Használat
A `mkdir` parancs alapvető szintaxisa a következő:

```bash
mkdir [opciók] [argumentumok]
```

## Gyakori Opciók
- `-p`: Létrehozza a megadott könyvtárat és a szülő könyvtárakat is, ha azok még nem léteznek.
- `-v`: Részletes kimenetet ad, amely megmutatja, hogy mely könyvtárakat hozta létre.
- `--mode`: Beállítja a könyvtár jogosultságait a létrehozáskor.

## Gyakori Példák
- Egy egyszerű könyvtár létrehozása:

```bash
mkdir uj_konyvtar
```

- Több könyvtár létrehozása egyszerre:

```bash
mkdir konyvtar1 konyvtar2 konyvtar3
```

- Szülő könyvtárakkal együtt történő létrehozás:

```bash
mkdir -p szulo_konyvtar/gyerek_konyvtar
```

- Részletes kimenet megjelenítése a létrehozás során:

```bash
mkdir -v uj_konyvtar
```

## Tippek
- Mindig ellenőrizd, hogy a könyvtár, amelyet létre szeretnél hozni, még nem létezik-e, hogy elkerüld a hibákat.
- Használj `-p` opciót, ha több szintű könyvtárat szeretnél létrehozni, mivel ez automatikusan létrehozza a szükséges szülő könyvtárakat.
- A `mkdir` parancs használatakor ügyelj a jogosultságokra, különösen, ha rendszergazdai jogosultságokkal dolgozol.