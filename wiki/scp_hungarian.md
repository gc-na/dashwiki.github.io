# [Debian] Debian Almquist Shell (dash) scp használata: Fájlok másolása távoli gépekre

## Áttekintés
Az `scp` (Secure Copy Protocol) parancs lehetővé teszi fájlok biztonságos másolását egy helyi gépről egy távoli gépre, vagy fordítva, SSH (Secure Shell) protokollon keresztül. Ez a parancs titkosítja a fájlokat és az adatokat, így védve a másolás során.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
scp [opciók] [forrás] [cél]
```

## Gyakori opciók
- `-r`: Rekurzív másolás mappák esetén.
- `-P`: A távoli gép portjának megadása (nagy P, mert a `-p` opció más funkciót lát el).
- `-i`: Az SSH kulcs fájl megadása.
- `-v`: Verbose (részletes) mód, amely több információt ad a másolás folyamatáról.

## Gyakori példák
1. Fájl másolása helyi gépről távoli gépre:
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. Fájl másolása távoli gépről helyi gépre:
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. Mappa rekurzív másolása távoli gépre:
   ```bash
   scp -r /path/to/local/directory user@remote_host:/path/to/remote/directory/
   ```

4. Fájl másolása egy nem alapértelmezett porton:
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tippek
- Mindig ellenőrizze, hogy a távoli gép elérhető-e, mielőtt fájlokat másolna.
- Használja a `-v` opciót a hibaelhárításhoz, ha problémák merülnek fel a másolás során.
- Ha gyakran használ SSH kulcsokat, érdemes lehet az `-i` opciót beállítani, hogy ne kelljen minden alkalommal megadni a kulcs fájlt.