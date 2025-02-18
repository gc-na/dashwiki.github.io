# [Deutsch] Debian Almquist Shell (dash) ftp Verwendung: Dateien über das FTP-Protokoll übertragen

## Übersicht
Der `ftp`-Befehl wird verwendet, um Dateien über das File Transfer Protocol (FTP) zu übertragen. Mit diesem Befehl können Benutzer sich mit einem FTP-Server verbinden, Dateien hoch- und herunterladen sowie Verzeichnisse auf dem Server durchsuchen.

## Verwendung
Die grundlegende Syntax des `ftp`-Befehls lautet:

```bash
ftp [Optionen] [Argumente]
```

## Häufige Optionen
- `-i`: Schaltet den interaktiven Modus aus, sodass die Übertragung ohne Bestätigungen erfolgt.
- `-n`: Verhindert die automatische Anmeldung beim FTP-Server.
- `-v`: Aktiviert den ausführlichen Modus, der mehr Informationen über den Verbindungsstatus anzeigt.

## Häufige Beispiele

### Verbindung zu einem FTP-Server herstellen
Um eine Verbindung zu einem FTP-Server herzustellen, verwenden Sie den folgenden Befehl:

```bash
ftp ftp.example.com
```

### Anmelden mit Benutzername und Passwort
Um sich mit einem bestimmten Benutzernamen und Passwort anzumelden, verwenden Sie:

```bash
ftp -n ftp.example.com
```
Nach der Verbindung können Sie den Befehl `user` verwenden, um sich anzumelden:

```bash
user meinBenutzername meinPasswort
```

### Dateien herunterladen
Um eine Datei vom FTP-Server herunterzuladen, verwenden Sie den Befehl `get`:

```bash
get datei.txt
```

### Dateien hochladen
Um eine Datei auf den FTP-Server hochzuladen, verwenden Sie den Befehl `put`:

```bash
put datei.txt
```

### Verzeichnisinhalt auflisten
Um den Inhalt des aktuellen Verzeichnisses auf dem FTP-Server aufzulisten, verwenden Sie:

```bash
ls
```

## Tipps
- Verwenden Sie den `-i`-Schalter, um die Übertragung zu automatisieren, insbesondere bei großen Dateien.
- Achten Sie darauf, sich nach der Verwendung von `ftp` abzumelden, um die Sicherheit zu gewährleisten.
- Nutzen Sie den `-v`-Schalter, um bei Verbindungsproblemen mehr Informationen zu erhalten.