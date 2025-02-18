# [Deutsch] Debian Almquist Shell (dash) umask Verwendung: Steuerung der Standardberechtigungen für neue Dateien

## Übersicht
Der `umask`-Befehl in der Debian Almquist Shell (dash) wird verwendet, um die Standardberechtigungen für neu erstellte Dateien und Verzeichnisse festzulegen. Er bestimmt, welche Berechtigungen beim Erstellen neuer Dateien und Verzeichnisse standardmäßig eingeschränkt werden.

## Verwendung
Die grundlegende Syntax des `umask`-Befehls lautet:

```sh
umask [Optionen] [Argumente]
```

## Häufige Optionen
- `-S`: Zeigt die aktuelle umask in symbolischer Form an.
- `N`: Setzt die umask auf den angegebenen Wert (z. B. `022`).

## Häufige Beispiele

1. **Aktuelle umask anzeigen**
   ```sh
   umask
   ```

2. **Umask auf einen bestimmten Wert setzen**
   ```sh
   umask 027
   ```

3. **Umask in symbolischer Form anzeigen**
   ```sh
   umask -S
   ```

4. **Umask für die aktuelle Sitzung ändern**
   ```sh
   umask 002
   ```

5. **Umask zurücksetzen auf Standardwert**
   ```sh
   umask 000
   ```

## Tipps
- Überprüfen Sie regelmäßig Ihre umask-Einstellungen, um sicherzustellen, dass neue Dateien die gewünschten Berechtigungen haben.
- Verwenden Sie eine restriktivere umask in sicherheitskritischen Umgebungen, um unbefugten Zugriff zu verhindern.
- Denken Sie daran, dass die umask nur die Standardberechtigungen für neue Dateien und Verzeichnisse beeinflusst; bestehende Dateien bleiben unverändert.