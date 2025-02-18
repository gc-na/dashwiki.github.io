# [Debian] Debian Almquist Shell (dash) sftp használata: Fájlok biztonságos átvitele

## Áttekintés
Az `sftp` (Secure File Transfer Protocol) parancs egy biztonságos fájlátviteli protokoll, amely lehetővé teszi a fájlok átvitelét egy távoli gép és a helyi gép között SSH (Secure Shell) kapcsolaton keresztül. Az `sftp` parancs titkosítja az adatokat, így biztonságosabb, mint a hagyományos FTP.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
sftp [opciók] [felhasználónév@]host
```

## Gyakori opciók
- `-P`: A port megadása, amelyen a szerver elérhető.
- `-o`: Különböző SSH beállítások megadása, például `-o StrictHostKeyChecking=no`.
- `-b`: Batch mód, amely lehetővé teszi a parancsok fájlból való végrehajtását.

## Gyakori példák
1. **Kapcsolódás egy távoli szerverhez**:
   ```bash
   sftp user@example.com
   ```

2. **Fájl letöltése a távoli szerverről**:
   ```bash
   sftp user@example.com
   get remote_file.txt
   ```

3. **Fájl feltöltése a távoli szerverre**:
   ```bash
   sftp user@example.com
   put local_file.txt
   ```

4. **Több fájl letöltése**:
   ```bash
   sftp user@example.com
   mget *.txt
   ```

5. **Mappa letöltése**:
   ```bash
   sftp user@example.com
   get -r remote_directory
   ```

## Tippek
- Mindig használj erős jelszót a távoli szerverhez való kapcsolódáskor.
- Használj SSH kulcsokat a jelszó nélküli bejelentkezéshez, hogy növeld a biztonságot.
- Ellenőrizd a távoli szerver hitelesítési kulcsát, hogy elkerüld a man-in-the-middle támadásokat.