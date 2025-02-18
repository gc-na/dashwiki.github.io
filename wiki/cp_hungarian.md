# [Debian] Debian Almquist Shell (dash) cp használata: Fájlok másolása

## Áttekintés
A `cp` parancs a fájlok és könyvtárak másolására szolgál a Debian Almquist Shell (dash) környezetében. Ez a parancs lehetővé teszi a felhasználók számára, hogy fájlokat másoljanak egyik helyről a másikra, megkönnyítve ezzel az adatok kezelését.

## Használat
A `cp` parancs alapvető szintaxisa a következő:

```
cp [opciók] [forrás] [cél]
```

## Gyakori opciók
- `-r`: Rekurzív másolás, könyvtárak másolására használják.
- `-i`: Interaktív mód, amely megerősítést kér, ha a célfájl már létezik.
- `-u`: Csak akkor másolja a fájlt, ha a forrás újabb, mint a cél.
- `-v`: Verbose, azaz részletes kimenetet ad, amely megmutatja, hogy mely fájlok kerültek másolásra.

## Gyakori példák
1. **Egyszerű fájl másolás:**
   ```bash
   cp file.txt backup_file.txt
   ```

2. **Könyvtár rekurzív másolása:**
   ```bash
   cp -r my_folder/ backup_folder/
   ```

3. **Fájl másolása megerősítéssel:**
   ```bash
   cp -i file.txt existing_file.txt
   ```

4. **Csak újabb fájlok másolása:**
   ```bash
   cp -u file.txt backup_file.txt
   ```

5. **Részletes másolás megjelenítése:**
   ```bash
   cp -v file.txt backup_file.txt
   ```

## Tippek
- Mindig használj `-i` opciót, ha nem vagy biztos abban, hogy a célfájl létezik, hogy elkerüld a véletlen felülírást.
- Használj `-r` opciót, ha könyvtárakat másolsz, hogy biztosítsd a tartalom teljes másolását.
- Ellenőrizd a fájlok másolásának eredményét a `-v` opcióval, hogy lásd, mi történt a parancs futtatása során.