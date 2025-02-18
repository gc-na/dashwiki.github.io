# [Debian] Debian Almquist Shell (dash) shift használat: Argumentumok eltolása

## Áttekintés
A `shift` parancs a shell környezetben az argumentumok eltolására szolgál. Ez lehetővé teszi, hogy a parancssori argumentumok listáját balra toljuk, így a `$1` változó a második argumentumra, a `$2` a harmadikra, és így tovább mutat.

## Használat
A `shift` parancs alapvető szintaxisa a következő:

```bash
shift [n]
```

Ahol `n` az eltolás mértéke (alapértelmezés szerint 1).

## Gyakori Opciók
- `n`: Az eltolás mértéke, amely megadja, hogy hány argumentumot szeretnénk eltoltni. Ha nem adunk meg értéket, akkor az alapértelmezett érték 1.

## Gyakori Példák
1. **Alapértelmezett eltolás**:
   ```bash
   # Eredeti argumentumok
   echo "Eredeti argumentumok: $1, $2, $3"
   shift
   echo "Eltolt argumentumok: $1, $2, $3"
   ```

2. **Több argumentum eltolása**:
   ```bash
   # Eredeti argumentumok
   echo "Eredeti argumentumok: $1, $2, $3, $4"
   shift 2
   echo "Eltolt argumentumok: $1, $2"
   ```

3. **Ciklus használata**:
   ```bash
   while [ "$#" -gt 0 ]; do
       echo "Aktuális argumentum: $1"
       shift
   done
   ```

## Tippek
- Használj `shift`-et ciklusokban, hogy könnyen feldolgozd az összes argumentumot.
- Ellenőrizd a `$#` változót, hogy megtudd, hány argumentum maradt a `shift` végrehajtása után.
- Légy óvatos a `shift` használatával, mivel az eltávolítja az argumentumokat, és azok később nem lesznek elérhetők.