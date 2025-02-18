# [Debian] Debian Almquist Shell (dash) rmdir használata: Üres könyvtárak törlése

## Áttekintés
A `rmdir` parancs a Debian Almquist Shell (dash) környezetben üres könyvtárak törlésére szolgál. Ha a megadott könyvtár nem üres, a parancs nem hajtja végre a törlést, és hibaüzenetet ad vissza.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
rmdir [opciók] [argumentumok]
```

## Gyakori opciók
- `--ignore-fail-on-non-empty`: A parancs figyelmen kívül hagyja a nem üres könyvtárakat, és nem ad vissza hibát.
- `--verbose`: Részletes kimenetet ad a törlés folyamatáról.

## Gyakori példák
1. Üres könyvtár törlése:
   ```bash
   rmdir pelda_konyvtar
   ```

2. Több üres könyvtár törlése egyszerre:
   ```bash
   rmdir konyvtar1 konyvtar2 konyvtar3
   ```

3. Üres könyvtár törlése hibakezeléssel:
   ```bash
   rmdir --ignore-fail-on-non-empty pelda_konyvtar
   ```

4. Részletes kimenet a törlésről:
   ```bash
   rmdir --verbose pelda_konyvtar
   ```

## Tippek
- Mindig ellenőrizd, hogy a törölni kívánt könyvtár üres-e, hogy elkerüld a hibákat.
- Használj `--verbose` opciót, ha szeretnéd látni, mi történik a törlés során.
- Ha nem vagy biztos a törlésben, használj más parancsokat, mint például `ls`, hogy megnézd a könyvtár tartalmát.