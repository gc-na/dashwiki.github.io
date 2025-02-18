# [Debian] Debian Almquist Shell (dash) curl használata: Webes adatok lekérése

## Áttekintés
A `curl` parancs egy parancssori eszköz, amely lehetővé teszi a webes erőforrások lekérését és kezelését különböző protokollokon keresztül, mint például HTTP, HTTPS, FTP és mások. Gyakran használják API-k elérésére és fájlok letöltésére.

## Használat
A `curl` parancs alapvető szintaxisa a következő:

```bash
curl [opciók] [argumentumok]
```

## Gyakori opciók
- `-O`: A fájl letöltése és mentése az eredeti néven.
- `-L`: Kövesse a HTTP átirányításokat.
- `-d`: Adatok küldése POST kérésekben.
- `-H`: Egyéni fejléc hozzáadása a kéréshez.
- `-I`: Csak a HTTP fejléc lekérése.

## Gyakori példák
1. **Weboldal letöltése**:
   ```bash
   curl http://example.com
   ```

2. **Fájl letöltése az eredeti néven**:
   ```bash
   curl -O http://example.com/file.zip
   ```

3. **HTTP fejléc lekérése**:
   ```bash
   curl -I http://example.com
   ```

4. **Adatok küldése POST kérésben**:
   ```bash
   curl -d "name=John&age=30" http://example.com/api
   ```

5. **Követés átirányításokkal**:
   ```bash
   curl -L http://example.com/redirect
   ```

## Tippek
- Mindig ellenőrizd a `curl` parancs kimenetét, hogy megbizonyosodj arról, hogy a lekérés sikeres volt.
- Használj `-o` opciót, ha szeretnéd megadni a letöltött fájl nevét.
- A `curl` parancs használata előtt érdemes megismerni az API dokumentációját, ha API-kat használsz.