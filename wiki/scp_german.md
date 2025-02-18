# [Deutsch] Debian Almquist Shell (dash) scp Verwendung: Dateien sicher kopieren

## Übersicht
Der `scp`-Befehl (Secure Copy Protocol) wird verwendet, um Dateien sicher zwischen Hosts über ein Netzwerk zu kopieren. Er nutzt SSH (Secure Shell) zur Authentifizierung und Verschlüsselung der Datenübertragung.

## Verwendung
Die grundlegende Syntax des `scp`-Befehls lautet:

```bash
scp [Optionen] [Quell] [Ziel]
```

## Häufige Optionen
- `-r`: Kopiert Verzeichnisse rekursiv.
- `-P`: Gibt den Port an, der für die SSH-Verbindung verwendet werden soll (großes P).
- `-p`: Bewahrt die Zeitstempel und Berechtigungen der Dateien.
- `-v`: Aktiviert den ausführlichen Modus, um Debugging-Informationen anzuzeigen.

## Häufige Beispiele
1. **Eine Datei von lokal nach remote kopieren:**
   ```bash
   scp /pfad/zur/datei.txt benutzer@remote-host:/pfad/zum/ziel/
   ```

2. **Eine Datei von remote nach lokal kopieren:**
   ```bash
   scp benutzer@remote-host:/pfad/zur/datei.txt /pfad/zum/ziel/
   ```

3. **Ein ganzes Verzeichnis rekursiv kopieren:**
   ```bash
   scp -r /pfad/zum/verzeichnis benutzer@remote-host:/pfad/zum/ziel/
   ```

4. **Eine Datei über einen bestimmten SSH-Port kopieren:**
   ```bash
   scp -P 2222 /pfad/zur/datei.txt benutzer@remote-host:/pfad/zum/ziel/
   ```

## Tipps
- Verwenden Sie `-v`, um Probleme bei der Verbindung zu diagnostizieren.
- Achten Sie darauf, dass der SSH-Dienst auf dem Zielhost läuft, um eine Verbindung herzustellen.
- Nutzen Sie SSH-Schlüssel für eine einfachere und sicherere Authentifizierung, anstatt Passwörter einzugeben.