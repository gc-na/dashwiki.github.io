# [Debian] Debian Almquist Shell (dash) batch használata: Feladatok ütemezése

## Áttekintés
A `batch` parancs lehetővé teszi, hogy a felhasználók ütemezett feladatokat futtassanak a rendszer terhelésének csökkentése érdekében. A parancs a háttérben fut, és a rendszer terheltségétől függően végzi el a megadott parancsokat.

## Használat
A `batch` parancs alapvető szintaxisa a következő:

```bash
batch [opciók] [argumentumok]
```

## Gyakori opciók
- `-f`: A megadott fájlban található parancsokat futtatja.
- `-l`: A parancsok végrehajtásához szükséges környezeti változók betöltése.
- `-q`: Csendes mód, amely nem ír ki üzeneteket a parancs végrehajtásáról.

## Gyakori példák
1. **Egyszerű parancs ütemezése**:
   A következő parancs a `date` parancsot ütemezi a háttérben való végrehajtásra.
   ```bash
   echo "date" | batch
   ```

2. **Fájlban tárolt parancsok futtatása**:
   Ha van egy `my_commands.sh` fájl, amely parancsokat tartalmaz, a következőképpen futtathatjuk:
   ```bash
   batch -f my_commands.sh
   ```

3. **Több parancs ütemezése**:
   Több parancsot is ütemezhetünk egyszerre:
   ```bash
   echo -e "echo 'Hello, World!'\necho 'This is a batch job.'" | batch
   ```

## Tippek
- Használja a `batch` parancsot, amikor a rendszer terhelése alacsony, hogy a feladatok gyorsabban végrehajtódjanak.
- Ellenőrizze a `at` parancsot is, ha pontos időpontban szeretne feladatokat ütemezni.
- A `batch` parancs kimenetét a felhasználó e-mail címére küldheti, ha a rendszer e-mail szolgáltatása be van állítva.