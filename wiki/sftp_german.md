# [Deutsch] Debian Almquist Shell (dash) sftp Verwendung: Dateien sicher übertragen

## Übersicht
Der `sftp`-Befehl (Secure File Transfer Protocol) wird verwendet, um Dateien sicher über ein Netzwerk zu übertragen. Er bietet eine sichere Verbindung zu einem entfernten Server und ermöglicht das Hoch- und Herunterladen von Dateien sowie die Verwaltung von Verzeichnissen.

## Verwendung
Die grundlegende Syntax des `sftp`-Befehls lautet:

```bash
sftp [optionen] [benutzer@host]
```

## Häufige Optionen
- `-P <port>`: Gibt den Port an, der für die Verbindung verwendet werden soll.
- `-i <datei>`: Gibt eine Datei mit einem privaten Schlüssel für die Authentifizierung an.
- `-o <option>`: Ermöglicht das Festlegen von SSH-Optionen.

## Häufige Beispiele
Um eine Verbindung zu einem SFTP-Server herzustellen, verwenden Sie den folgenden Befehl:

```bash
sftp benutzer@host
```

Um eine Datei von Ihrem lokalen System auf den Server hochzuladen, verwenden Sie:

```bash
put lokale_datei.txt
```

Um eine Datei vom Server auf Ihr lokales System herunterzuladen, verwenden Sie:

```bash
get entfernte_datei.txt
```

Um ein Verzeichnis auf dem Server zu wechseln, verwenden Sie:

```bash
cd /pfad/zum/verzeichnis
```

Um eine Liste der Dateien im aktuellen Verzeichnis anzuzeigen, verwenden Sie:

```bash
ls
```

## Tipps
- Verwenden Sie den `-P`-Schalter, wenn der SFTP-Server einen anderen Port als den Standardport 22 verwendet.
- Nutzen Sie SSH-Schlüssel für eine sicherere Authentifizierung anstelle von Passwörtern.
- Überprüfen Sie regelmäßig die Berechtigungen Ihrer Dateien und Verzeichnisse auf dem Server, um die Sicherheit zu gewährleisten.