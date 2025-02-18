# [Debian] Debian Almquist Shell (dash) ftp használata: Fájlok átvitele FTP-n keresztül

## Áttekintés
Az `ftp` parancs egy fájlátviteli protokoll, amely lehetővé teszi fájlok küldését és fogadását egy távoli szerverről FTP (File Transfer Protocol) segítségével. Az `ftp` parancs használatával egyszerűen csatlakozhatunk FTP szerverekhez, navigálhatunk a könyvtárak között, és fájlokat tölthetünk le vagy fel.

## Használat
A `ftp` parancs alapvető szintaxisa a következő:

```bash
ftp [opciók] [argumentumok]
```

## Gyakori opciók
- `-i`: Kikapcsolja az interaktív módot, így nem kér megerősítést a fájlok átvitele előtt.
- `-v`: Verbózus mód, amely részletesebb információt ad az átvitel során.
- `-n`: Megakadályozza az automatikus bejelentkezést a szerverre.
- `-p`: Passzív mód, amely segít a tűzfalak mögötti kapcsolatokban.

## Gyakori példák
### 1. Kapcsolódás egy FTP szerverhez
```bash
ftp ftp.example.com
```

### 2. Fájl letöltése a szerverről
```bash
get file.txt
```

### 3. Fájl feltöltése a szerverre
```bash
put file.txt
```

### 4. Könyvtár listázása a szerveren
```bash
ls
```

### 5. Kilépés az FTP-ből
```bash
bye
```

## Tippek
- Mindig használjon biztonságos FTP-t (SFTP) érzékeny adatok átvitelére.
- Ellenőrizze a fájlok integritását a letöltés után, például MD5 hash segítségével.
- Használjon passzív módot, ha problémái vannak a tűzfalakkal vagy a NAT-tal.