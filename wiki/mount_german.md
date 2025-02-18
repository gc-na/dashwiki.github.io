# [Deutsch] Debian Almquist Shell (dash) mount Verwendung: [Dateisysteme einbinden]

## Übersicht
Der Befehl `mount` wird verwendet, um Dateisysteme in das Verzeichnisbaum des Systems einzubinden. Dies ermöglicht den Zugriff auf Dateien und Verzeichnisse, die auf verschiedenen Speichermedien oder Partitionen gespeichert sind.

## Verwendung
Die grundlegende Syntax des `mount`-Befehls lautet:

```
mount [Optionen] [Argumente]
```

## Häufige Optionen
- `-t <typ>`: Gibt den Typ des Dateisystems an (z.B. ext4, ntfs).
- `-o <Optionen>`: Ermöglicht das Setzen spezifischer Optionen wie `ro` (read-only) oder `rw` (read-write).
- `-a`: Bindet alle Dateisysteme ein, die in der Datei `/etc/fstab` aufgeführt sind.
- `-r`: Bindet das Dateisystem im Nur-Lese-Modus ein.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `mount`-Befehls:

1. **Einbinden eines ext4-Dateisystems:**
   ```bash
   mount -t ext4 /dev/sda1 /mnt/meinlaufwerk
   ```

2. **Einbinden eines NTFS-Dateisystems im Nur-Lese-Modus:**
   ```bash
   mount -t ntfs -o ro /dev/sdb1 /mnt/usb
   ```

3. **Einbinden aller in /etc/fstab definierten Dateisysteme:**
   ```bash
   mount -a
   ```

4. **Einbinden eines Dateisystems mit spezifischen Optionen:**
   ```bash
   mount -t ext4 -o rw,noatime /dev/sda2 /mnt/daten
   ```

## Tipps
- Überprüfen Sie immer, ob das Zielverzeichnis existiert, bevor Sie ein Dateisystem einbinden.
- Verwenden Sie `umount`, um ein eingebundenes Dateisystem sicher zu trennen.
- Achten Sie darauf, dass Sie die richtigen Berechtigungen haben, um ein Dateisystem einzubinden, da dies oft Administratorrechte erfordert.