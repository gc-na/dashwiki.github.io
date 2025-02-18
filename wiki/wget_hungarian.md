# [Debian] Debian Almquist Shell (dash) wget használata: Fájlok letöltése az internetről

## Áttekintés
A `wget` egy parancssori eszköz, amely lehetővé teszi fájlok letöltését az internetről. Képes HTTP, HTTPS és FTP protokollokon keresztül letölteni tartalmakat, és támogatja a folytatható letöltéseket is.

## Használat
A `wget` parancs alapvető szintaxisa a következő:

```bash
wget [opciók] [argumentumok]
```

## Gyakori Opciók
- `-O [fájl]`: A letöltött fájl nevét megadja.
- `-c`: Folyatatja a megszakított letöltéseket.
- `-q`: Csendes mód, nem jelenít meg kimenetet.
- `--limit-rate=[sebesség]`: Korlátozza a letöltési sebességet.
- `-r`: Rekurzív letöltés, mappák és fájlok letöltése.

## Gyakori Példák
1. **Egyszerű fájl letöltése:**
   ```bash
   wget https://example.com/file.zip
   ```

2. **Fájl letöltése egy adott névvel:**
   ```bash
   wget -O új_fájl.zip https://example.com/file.zip
   ```

3. **Letöltés folytatása:**
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. **Csendes mód használata:**
   ```bash
   wget -q https://example.com/file.zip
   ```

5. **Rekurzív letöltés:**
   ```bash
   wget -r https://example.com/directory/
   ```

## Tippek
- Használj `-c` opciót, ha nagy fájlokat töltesz le, hogy elkerüld a letöltés megszakadását.
- A `--limit-rate` opcióval szabályozhatod a sávszélességet, ha más feladatokat is végzel a hálózaton.
- Csendes módban a `-q` opcióval elkerülheted a felesleges kimeneteket, különösen, ha szkriptekben használod a `wget`-et.