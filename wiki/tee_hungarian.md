# [Debian] Debian Almquist Shell (dash) tee használata: Az adatok másolása és megjelenítése

## Áttekintés
A `tee` parancs lehetővé teszi, hogy a standard bemenetet (stdin) egyszerre írja ki a standard kimenetre (stdout) és egy vagy több fájlba. Ez hasznos, ha szeretnénk látni a parancs kimenetét, miközben azt egy fájlba is mentjük.

## Használat
A `tee` parancs alapvető szintaxisa a következő:

```bash
tee [opciók] [fájlok]
```

## Gyakori opciók
- `-a` vagy `--append`: A kimenetet a fájl végéhez fűzi, nem felülírja azt.
- `-i` vagy `--ignore-interrupts`: Figyelmen kívül hagyja a megszakítási jeleket.
- `--help`: Megjeleníti a parancs használati útmutatóját.

## Gyakori példák
1. **Kimenet megjelenítése és fájlba írás:**
   ```bash
   echo "Hello, World!" | tee output.txt
   ```
   Ez a parancs megjeleníti a "Hello, World!" üzenetet a képernyőn, és egyben elmenti az `output.txt` fájlba is.

2. **Kimenet hozzáfűzése egy meglévő fájlhoz:**
   ```bash
   echo "Another line" | tee -a output.txt
   ```
   Ez a parancs hozzáfűzi az "Another line" szöveget az `output.txt` fájl végéhez, miközben megjeleníti azt a képernyőn.

3. **Több fájlba írás:**
   ```bash
   echo "Logging data" | tee file1.txt file2.txt
   ```
   Ez a parancs a "Logging data" szöveget egyszerre írja az `file1.txt` és `file2.txt` fájlokba, miközben a kimenetet a képernyőn is megjeleníti.

## Tippek
- Használja a `-a` opciót, ha szeretné megőrizni a meglévő fájl tartalmát, és új adatokat szeretne hozzáfűzni.
- A `tee` parancsot gyakran használják csővezetékekben, hogy a parancsok kimenetét több helyen is felhasználhassák.
- Ha nem szeretné, hogy a `tee` megszakításokat vegyen figyelembe, használja az `-i` opciót.